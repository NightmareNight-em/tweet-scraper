## A crawler to scrape tweets - 100% working - 2023 Version 1.0.0

<h1>Twitter Scraper</h1>

  <p>Recently, Twitter has banned almost every Twitter scraper. This report presents an alternative tool to scrape Twitter.</p>

  <p>It is also possible to download the images shown in tweets by passing the argument <code>save_images = True</code>.</p>

  <p>If you only want to scrape images, it is recommended to set the argument <code>display_type = image</code> to show only tweets that contain images.</p>

  <h2>1. Pre-Requisites</h2>

  <ul>
      <li>Unzip the file into a project directory.</li>
      <li>Install Python 3.x.x and pip for python package installations.</li>
      <li>Twitter account authentication is required. It is recommended to log in with a new account, otherwise the account could be banned if extensive scraping is done. To log in to your account, you need to write your username USERNAME, password PASSWORD and mail ID EMAIL in the <code>.env</code> file.</li>
      <ol>
          <li>Go to the project directory in your terminal.</li>
          <li>Create <code>constants.py</code> file.</li>
          <li>Write below values -
              <ul>
                  <li><code>EMAIL=your_mail</code></li>
                  <li><code>PASSWORD=your_password</code></li>
                  <li><code>USERNAME=your_username</code></li>
              </ul>
          </li>
          <li>Save the file.</li>
      </ol>
  </ul>

  <h2>2. Usage</h2>

  <h3>Terminal</h3>

  <p><strong>Optional Argument Description</strong></p>

  <ul>
      <li><code>-h, --help</code>: Show this help message and exit</li>
      <li><code>--words WORDS</code>: Words to search for. They should be separated by "//": Cat//Dog.</li>
      <li><code>--from_account FROM_ACCOUNT</code>: Tweets posted by "from_account" account.</li>
      <li><code>--to_account TO_ACCOUNT</code>: Tweets posted in response to "to_account" account.</li>
      <li><code>--mention_account MENTION_ACCOUNT</code>: Tweets that mention "mention_account" account.</li>
      <li><code>--hashtag HASHTAG</code>: Tweets containing #hashtag</li>
      <li><code>--until UNTIL</code>: End date for search query. Example: %Y-%m-%d.</li>
      <li><code>--since SINCE</code>: Start date for search query. Example: %Y-%m-%d.</li>
      <li><code>--interval INTERVAL</code>: Interval days between each start date and end date for search queries. Example: 5.</li>
      <li><code>--lang LANG</code>: Tweets language. Example: "en" for English and "fr" for French.</li>
      <li><code>--headless HEADLESS</code>: Headless webdriver or not. True or False</li>
      <li><code>--limit LIMIT</code>: Limit tweets to be scrapped.</li>
      <li><code>--display_type DISPLAY_TYPE</code>: Display type of Twitter page: Latest or Top tweets</li>
      <li><code>--resume RESUME</code>: Resume the last scraping. Specify the CSV file path.</li>
      <li><code>--proxy PROXY</code>: Proxy server</li>
      <li><code>--proximity PROXIMITY</code>: Proximity</li>
      <li><code>--geocode GEOCODE</code>: Geographical location coordinates to center the search (), radius. Not compatible with proximity</li>
      <li><code>--minretweets MINRETWEETS</code>: Min. number of retweets</li>
      <li><code>--minlikes MINLIKES</code>: Min. number of likes to the tweet</li>
  </ul>

  <h2>3. Run Script On Terminal</h2>

  <p><strong>Example 1</strong></p>

  <pre>
  <code>python tweet_scraper.py --words "excellente//car" --until 2020-01-05 --since 2020-01-01 --limit 10 --interval 1 --display_type Latest --lang="en" --headless True</code>
  </pre>

  <p><strong>Example 2</strong></p>

  <pre>
  <code>python scweet.py --hashtag "bitcoin" --until 2020-01-05 --since 2020-01-01 --limit 10 --interval 1 --display_type Latest --lang="en" --headless True</code>
  </pre>

  <p>Change <code>--until</code> and <code>--since</code> to give a date range for tweets to be extracted. There are other modes too where you may set accounts from where tweets are posted or to whose response tweets were made. Additionally, you may set an account which is mentioned in the tweets. This way you can filter your extracted tweets up. Check Usage. Choose an interval that can divide the period of time between the start and max date.</p>

  <h2>4. Results</h2>

  <p>A CSV file is saved in a folder named 'outputs' in the project directory by itself. The CSV file contains the following features (for each tweet):</p>

  <ul>
      <li>'UserScreenName'</li>
      <li>'UserName'</li>
      <li>'Timestamp': Timestamp of the tweet</li>
      <li>'Text': Tweet text</li>
      <li>'Embedded_text': Embedded text written above the tweet. This can be an image, a video, or even another tweet if the tweet in question is a reply</li>
      <li>'Emojis': Emojis in the tweet</li>
      <li>'Comments': Number of comments</li>
      <li>'Likes': Number of likes</li>
      <li>'Retweets': Number of retweets</li>
      <li>'Image link': Link of the image in the tweet</li>
      <li>'Tweet URL': Tweet URL</li>
  </ul>

  <p>You will see references to CSV files in the 'outputs' folder in the zip file.</p>

  <h2>5. Developer’s Comments</h2>

  <p>The scraper has taken reference from a <a href="https://github.com/Altimis/Scweet/tree/master">git repository</a>. The latest code commit was a year ago so I had to make a lot of code changes. Also, the repository offers a python library to scrape tweets, which after testing, seems to be broken. Therefore, I needed to download some relevant files and make code changes wherever necessary. Also, scrapers tend to break when the HTML of the site changes so I will need to fix it as and when necessary in the future.</p>

<p>Thank You.</p>



