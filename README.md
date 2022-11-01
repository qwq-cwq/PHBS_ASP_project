# PHBS_ASP_project

This is the final project of PHBS ASP course, 2022 Fall Module 1. 

- Instructor: Prof. Jaehyuk Choi

- Course Website: [PHBS Applied Stochastic Processes](https://github.com/PHBS/ASP)

### Project description

The project is to pricing Snowball product using Monte Carlo methods. 

- Snowball products: provide the pricing function for standard snowball, "standard snowball" means the snowball option with both knock in bound and knock out bound, and the payout pattern should be: 
  - if knock out, then investor receive the coupon and the products matures prior to maturity; 
  - if knock in, the investor will:
    -  receive the coupon and the products matures prior to maturity if later knock out happens;
    - receive nothing if not knock out and the price of underlying asset exceeds the initial price at the last observation date. 
    - suffer a loss of $S_T-S_0$ if the  price of underlying is below the initial price at the last observation date. 
  - If neither knock-in nor knock-out happens, the investor can receive all the coupon until maturity. 
- The knock out is observed every month, knock in is observed every day. 
- Pricing models: the price is calculated using MC method. Two models are used to generate the paths of underlying assets, BS model and Heston Model. 

### Folders

- pyfeng: the folder contains one `snowball.py`, contains the codes for pricing snowball option.  
- snowball_docs: the folder contains the documents needed in our project presentation. 
  - `snowball_v2.ipynb` is the final report notebook. The final report implements the pricing functions in `pyfeng\snowball.py`, and calculated the price of snowball linked to CSI500.  
  -  `000905_close_price.xlsx` is the the closing price of CSI500. 
  - `IV_with_different_strike_1Y.xlsx` is the 1 year implied volatility (IV) of CSI500ETF option downloaded from Wind with different strikes. 
  - `500ETF_close_price.xlsx` is the close price of CSI500ETF. We assume the IV of CSI500 and CSI500 ETF should be similar. 
  - `picture` folder contains the pictures used in final report `snowball_v2.ipynb`. 

