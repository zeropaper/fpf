# FPF

Forkable Playlist Format


# Aims and goals

Provide a nerdy way to share links to media using source version control.


# How 

Based on structured text formats like JSON, XML or YAML and Git.


# Why

Why not?
But more seriously, git can be used to transfer files (with a variety of protocols, like SSH or HTTPS), can keep
tracks of changes and links can be made between repositories.


# Structure

```json
{
  "_links": {
    "repository": {
      "href": "..."
    }
  },
  "_embedded": {
    "media": [
      {
        "provider": "youtube",
        "provider_url": "Tu2_9L1Qp20"
      },
      {
        "provider": "vimeo",
        "provider_url": "Tu2_9L1Qp20"
      },
      {
        "provider": "url",
        ""
      }
    ],
    "provider": [
      {
        "name": "vimeo",
        "oembed": true
      }
    ]
  },
  "items": [
    
  ]
}

```


# Links

- [JSON](//json.org)
- [YAML](//yaml.org)
- [Git](//git-scm.com)
