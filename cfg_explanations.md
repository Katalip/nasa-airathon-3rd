Clarification about parameters in config files (on an example of train.yml)
Only parameters in **bold** should be changed if necessary. 

aod_and_gfs_filename: train_desc_aod_and_meteo_vars_11.03.csv       <- final view with merged aod and gfs
aod_csv_filename: merged_aod_desc_cwv_train_10.03.csv               <- final view with aod parameters only
city_mean_enc_mappings: models/saved_encodings/city_mean_enc_mappings_02.04_joblib.pkl <- mean encoding values computed from train set
                                                                                          for each city in case of new grid cells  
global_mean_enc: models/saved_encodings/global_mean_enc.txt          <- global mean encoding value in case if there is a new location 
le_mappings: models/saved_encodings/le_mappings_02.04_joblib.pkl     <- label encoder values computed from train set   
mean_enc_mappings: models/saved_encodings/mean_enc_mappings_02.04_joblib.pkl <- mean encoding values computed from train set
                                                                                for each grid id
order_of_columns: models/order_of_columns.txt                                <- order of features in the view models receive 
path_gfs_save_merged: data/interm/gfs/merged_csv                             <- folder for intermediate processing of GFS. Stores     
                                                                                merged csv files of grib files for group 1 and 2 for each city separately   
**path_grid_metadata**: data/raw/aod/grid_metadata.csv      <- path to the grid_metadata.csv (Same as in the competition)    
**path_labels**: data/raw/aod/train_labels.csv              <- path to the train_labels.csv or submission_format.csv (Same as in the 
                                                                                                                      competition)
path_maiac_assembled_csv: data/interm/maiac/assembled_csv/train    <- folder for intermediate processing of MAIAC
path_maiac_extracted_vars: data/interm/maiac/extracted_vars/train  <- folder for intermediate processing of MAIAC
**path_maiac_hdf_files**: data/raw/aod/train/maiac                 <- root path for the raw hdf files. Further splitted by years 
**path_raw_gfs**: data/raw/gfs/downloaded_files                    <- root path for the raw GFS files
**path_save_final_view**: data/processed                           <- where final views are saved 
path_shapefiles: data/interm/shape_files                           <- shape files created from grid_metadata.csv necessary for subsetting 
                                                                    hdf files  
period_name: train                                                 <- name of the config file 
**run_in_parallel**: true                                          <- option to run maiac preprocessing using multiprocessing. The loop 
                                                                      versions of the methods are available 
saved_final_gbr_model: models/grb_winning_02.04_joblib.pkl         <- serialized final Gradient Boosting Regressor model
saved_final_rf_model: models/rf_winning_02.04_joblib.pkl           <- serialized final Random Forest Regressor model 