# utl-scrape-weather-conditions-for-a-past-march-red-sox-vs-orioles-game-
    %let pgm=utl-scrape-weather-conditions-for-a-past-march-red-sox-vs-orioles-game;

    Scrape weather conditions for past march red sox vs orioles game

    github
    https://tinyurl.com/m8cae749
    https://github.com/rogerjdeangelis/utl-scrape-weather-conditions-for-a-past-march-red-sox-vs-orioles-game-

    related repos on end

    see
    Problem scrapping web page
    http://stackoverflow.com/questions/43466134/problems-with-scraping-webpage

    chinsoon12 profile
    http://stackoverflow.com/users/1989480/chinsoon12

    /*                   _
    (_)_ __  _ __  _   _| |_
    | | `_ \| `_ \| | | | __|
    | | | | | |_) | |_| | |_
    |_|_| |_| .__/ \__,_|\__|
            |_|
    */

    /**************************************************************************************************************************/
    /* http://www.baseball-reference.com/boxes/BAL/BAL201403310.shtml                                                         */
    /**************************************************************************************************************************/

    /*
     _ __  _ __ ___   ___ ___  ___ ___
    | `_ \| `__/ _ \ / __/ _ \/ __/ __|
    | |_) | | | (_) | (_|  __/\__ \__ \
    | .__/|_|  \___/ \___\___||___/___/
    |_|
    */

    %symdel want / nowarn;

    %utl_submit_r64('
    library(rvest);
    lines <- readLines(
     "http://www.baseball-reference.com/boxes/BAL/BAL201403310.shtml");
     want <- read_html(lines[which(grepl("Start Time Weather",lines))]) %>%
        html_node("div") %>%
        html_text();
     writeClipboard(want);
    ',return=want);

    %put &=want;


    /**************************************************************************************************************************/
    /*                                                                                                                        */
    /* Very simple process                                                                                                    */
    /* Read the line that contains the string 'Start Time Weather' from the html                                              */
    /* Format line and snd to the windows clipboard                                                                           */
    /*                                                                                                                        */
    /* Here is the line                                                                                                       */
    /* <div><strong>Start Time Weather:</strong> 60&deg; F, Wind 19mph from Right to Left, Sunny.</div>                       */
    /*                                                                                                                        */
    /**************************************************************************************************************************/

    /*           _               _
      ___  _   _| |_ _ __  _   _| |_
     / _ \| | | | __| `_ \| | | | __|
    | (_) | |_| | |_| |_) | |_| | |_
     \___/ \__,_|\__| .__/ \__,_|\__|
                    |_|
    */

    /**************************************************************************************************************************/
    /*                                                                                                                        */
    /*  The R script creates the sas macro variable want                                                                      */
    /*                                                                                                                        */
    /*  %put &=want;                                                                                                          */
    /*                                                                                                                        */
    /*  WANT=Start Time Weather: 60° F, Wind 19mph from Right to Left, Sunny.                                                 */
    /*                                                                                                                        */
    /**************************************************************************************************************************/


    REPO
    ------------------------------------------------------------------------------------------------------------------------------------
    https://github.com/rogerjdeangelis/utl-Web-Scraping-data-from-Australian-Open-stats
    https://github.com/rogerjdeangelis/utl-identifying-html-nodes-and-extracting-specific-information-scraping-html
    https://github.com/rogerjdeangelis/utl-identifying-the-html-table-and-exporting-to-spss-then-sas-scraping
    https://github.com/rogerjdeangelis/utl-locating-the-html-node-and-web-scrape-the-html-table
    https://github.com/rogerjdeangelis/utl-scraping-a-single-indirect-html-reference-using-python-beautiful-soup-and-request-packages
    https://github.com/rogerjdeangelis/utl-scraping-pdf-output-for-pdf-tables-and-lists
    https://github.com/rogerjdeangelis/utl-scraping-server-screens-when-Copy-Print-PageSource-are-disabled-python-tesseract
    https://github.com/rogerjdeangelis/utl-web-scaping-Loop-over-many-URLs-scrape-parse-extract-nodes-and-put-into-a-sas-table
    https://github.com/rogerjdeangelis/utl-web-scraping-USDOT-vehicle-inspections-and-fatalities
    https://github.com/rogerjdeangelis/utl-web-scraping-a-large-wikipedia-html-table-user-R-rvest
    https://github.com/rogerjdeangelis/utl-web-scraping-spains-grananda-soccer-team-players
    https://github.com/rogerjdeangelis/utl_scrape_javascript_converting_table_to_sas_dataset_no_browser
    https://github.com/rogerjdeangelis/utl_scraping_javascript_generated_html_web_pages
    https://github.com/rogerjdeangelis/utl_scraping_mutiple_web_tables_and_creating_seven_database_tables
    https://github.com/rogerjdeangelis/utl_web_scrape_23_separate_pages_one_per_state_for_all_whole_food_store_addresses
    https://github.com/rogerjdeangelis/utl_web_scraping_programatically_using_a_web_search_box_and_retrieve_information
    https://github.com/rogerjdeangelis/utl_web_scraping_top_cnn_stories
    https://github.com/rogerjdeangelis/utl_web_scraping_web_pages_for_the_latest_news_on_the_food_shortage_in_yemen
    https://github.com/rogerjdeangelis/utl_webscraping_www.treasury.gov__xml_page_of_interest_rates

    /*              _
      ___ _ __   __| |
     / _ \ `_ \ / _` |
    |  __/ | | | (_| |
     \___|_| |_|\__,_|

    */
Scrape weather conditions for past march red sox vs orioles game
