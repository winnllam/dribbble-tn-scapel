![dribbble-tn-scapel](https://user-images.githubusercontent.com/36285522/94328961-f0dcf580-ff84-11ea-856a-5716fdfa988d.png)


# Dribbble Thumbnail Extractor - REST API

An API that extracts thumbnail URLs of shots made by a user on [Dribbble](https://dribbble.com/winnllam). This enables the user to display their creative pieces in different locations while only posting on one.

## Table of Contents

* [Usage](https://github.com/winnllam/dribbble-tn-scapel#usage)
* [Technologies](https://github.com/winnllam/dribbble-tn-scapel#technologies)
    * [Installation](https://github.com/winnllam/dribbble-tn-scapel#Installation) (Development purposes)
    * [Deployment](https://github.com/winnllam/dribbble-tn-scapel#Deployment)
* [Use Cases](https://github.com/winnllam/dribbble-tn-scapel#Use-Cases)
* [Sources](https://github.com/winnllam/dribbble-tn-scapel#sources)

## Usage

Currently accessible at: https://dribbble-tn.herokuapp.com/

Checkout the documentation in [Postman](https://explore.postman.com/templates/13168/dribbble-thumbnail-api).

### [GET] get_img_urls

Gets the thumbnail image link for a user on Dribbble. Example call [here](https://dribbble-tn.herokuapp.com/get_img_urls/?name=winnllam).

#### Input
Parameter: name (the username of the Dribbble user)  
Example: `/get_img_urls/?name=winnllam`

#### Return
List of thumbnail image links in a JSON format  
Example:
```
{"urls":
  ["https://cdn.dribbble.com/users/4414719/screenshots/14252062/untitled_artwork_1x.png",
  "https://cdn.dribbble.com/users/4414719/screenshots/14150835/img_0162_1x.png",
  "https://cdn.dribbble.com/users/4414719/screenshots/14067337/img_0159_1x.jpg"]
}
```

## Technologies

* Python (BeautifulSoup4)
* Flask
* Heroku
* Postman

### Installation

You will need Python to be able to run the code.

Clone the repository and create your virtual environment:
```
python -m venv venv/
```

Activate the virtual environment:
```
source venv/scripts/activate
```

Run the code on [localhost](http://127.0.0.1:5000/) (port 5000):
```
python app.py
```

#### Collection

You can download the collection in Postman [here](https://explore.postman.com/templates/13168/dribbble-thumbnail-api). Click **Run in Postman** to start it up.

### Deployment

Make sure you have a created app on Heroku to deploy to.

Associate your project name on Heroku to your repository:
```
heroku git:remote -a {your-heroku-app-name}
```

Push to Heroku:
```
git push heroku master
```

Your endpoint is good to go!

## Use Cases

* Display them on your [website](https://winnllam.github.io/media) 

## Sources
* https://stackabuse.com/deploying-a-flask-application-to-heroku/
