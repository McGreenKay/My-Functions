def read_arff(file_name_or_link):
    
    """ 
    The function reads an arff file to dataframe
    
    Parameters
    ----------
    file_name_or_link: str
    The name or local path to the arff file
    
    Return
    ------
    A dataframe of the arff file
    
    Requirement
    -----------
    Installation of scipy library
    
    """
    # import pandas library as pd
    import pandas as pd 
    
    # import arff module from scipy.io
    from scipy.io import arff
    
    # read the arff using loadarff method
    arff_file = arff.loadarff(file_name_or_link)
    
    # read the arff into dataframe
    arff_file_df = pd.DataFrame(arff_file)
    
    return arff_file_df
