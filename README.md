# FPF

Forkable Playlist Format


# Aims and goals

Provide a nerdy way to share links to web viewable media using source version control or HTTP(S).


# How 

Based on structured text formats like JSON or XML, Git and when available oEmbed linking.


# Why

Why not?
But more seriously, git can be used to transfer files (with a variety of protocols, like SSH or HTTPS), can keep
tracks of changes and links can be made between repositories.


# Structure

The structure of a fpf file should limit redundancies and this is why HAL way of structuring data is used.


```json
{
  "_links": {
    "curies": [
      {
        "name": "youtube",
        "href": "http://www.youtube.com/oembed?url={rel}?format=json",
        "templated": true
      },
      {
        "name": "vimeo",
        "href": "http://vimeo.com/api/oembed.json?url={rel}",
        "templated": true
      }
    ],
    "repository": {
      "href": "..."
    },
    "youtube:some-other-media-id": {
    },
    "vimeo:some-media-id": {
      "href": ""
    }
  },
  "items": [
    "some-media-id",
    "some-other-media-id"
  ]
}

```


# Links

- [HAL](//stateless.co/hal_specification.html)
- [JSON](//json.org)
- [YAML](//yaml.org)
- [Git](//git-scm.com)
- [oEmbed](//oembed.com)
