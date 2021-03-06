# Overview

```
Module Name: AdKernel Bidder Adapter
Module Type: Bidder Adapter
Maintainer: prebid-dev@adkernel.com
```

# Description

Connects to AdKernel whitelabel platform.
Banner, video and native formats are supported.


# Test Parameters
```
var adUnits = [{
  code: 'banner-ad-div',
  mediaTypes: {
    banner: {
      sizes: [[300, 250]], // banner size
    }
  },
  bids: [{
    bidder: 'adkernel',
    params: {
      zoneId: '30164', //required parameter
      host: 'cpm.metaadserving.com' //required parameter
    }
  }]
}, {
  code: 'video-ad-player',
  mediaTypes: {
    video: {
      context: 'instream', // or 'outstream'
      playerSize: [640, 480] // video player size
    }
  },
  bids: [{
    bidder: 'adkernel',
    params: {
      zoneId: '30164', //required parameter
      host: 'cpm.metaadserving.com' //required parameter
    }
  }]
}, {
  code: 'native-ad',
  mediaTypes: {
    native: {
      title: {
        required: true
      },
      body: {
        required: true
      },
      icon: {
        required: true,
        size: [64, 64]
      },
      sponsoredBy: {
        required: true
      },
      clickUrl: {
        required: true
      },
      displayUrl: {
        required: false
      }
    }
  },
  bids: [{
    bidder: 'adkernel',
    params: {
      host: 'cpm.metaadserving.com',
      zoneId: 30164
    }
  }]
}];
```
