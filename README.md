metrics
=======

A Custom Metrics Collection/Reporting App

Base url = metrics.teagles.io/v1

Create a project

post /projects
```
  {
    api_key: '4nb2458fnq04b0anc94adksjfk',
    name: 'Awesome Project'
  }
```

Response
```
{
  project: {
    name:  'Awesome Project',
    id: '5317dfb3ed339cb42d000003'
  }
}
```

Create an Event

post /projects/5317dfb3ed339cb42d000003/events
```
  {
    name: 'WebInquirySubmitted',
      properties {
        full_name: 'John Smith',
        company: 'ACME Co.',
        email: 'john@acme.io'
      }
  }
```

post /projects/5317dfb3ed339cb42d000003/events/bulk
```
  {
    [
      {
        name: 'WebInquirySubmitted',
        properties {
          full_name: 'John Smith',
          company: 'ACME Co.',
          email: 'john@acme.io'
        }
      },
      {
        name: 'WebInquirySubmitted',
        properties {
          full_name: 'Billy Bob',
          company: 'Big Bucks',
          email: 'billy@bob.io'
        }
      }
  }

  
