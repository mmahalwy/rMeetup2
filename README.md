# rMeetup2

A Ruby gem to access the Meetup API 2. For now, this is very simple but I wish to implement new features in the future.

## Code Sample

```ruby
RMeetup2::Client.api_key= "YOUR API KEY"
results = RMeetup2::Request.new(:categories).execute()
results.each do |result|
  puts result["name"] #or something else
end
```

You can also add parameters like this :
```ruby
results = RMeetup2::Request.new(:cities, {:page => "5"}).execute()
```

Possible data models :
* `:categories` ([API doc](http://www.meetup.com/meetup_api/docs/2/categories/))
* `:checkins` ([API doc](http://www.meetup.com/meetup_api/docs/2/checkins/))
* `:cities` ([API doc](http://www.meetup.com/meetup_api/docs/2/cities/))
* `:events` ([API doc](http://www.meetup.com/meetup_api/docs/2/events/))
* `:groups` ([API doc](http://www.meetup.com/meetup_api/docs/2/groups/))
* `:groups3` ([API doc](http://www.meetup.com/meetup_api/docs/find/groups/))
* `:topics` ([API doc](http://www.meetup.com/meetup_api/docs/topics/))
* `:members` ([API doc](http://www.meetup.com/meetup_api/docs/2/members/))
* `:rsvps` ([API doc](http://www.meetup.com/meetup_api/docs/2/rsvps/))

## Contributing to rMeetup2
             
* Check out the latest master to make sure the feature hasn't been implemented or the bug hasn't been fixed yet.
* Check out the issue tracker to make sure someone already hasn't requested it and/or contributed it.
* Fork the project.
* Start a feature/bugfix branch.
* Commit and push until you are happy with your contribution.
* Make sure to add tests for it. This is important so I don't break it in a future version unintentionally.
* Please try not to mess with the Rakefile, version, or history. If you want to have your own version, or is otherwise necessary, that is fine, but please isolate to its own commit so I can cherry-pick around it.

## Copyright

Copyright (c) 2013 Antoine Menini. See LICENSE.txt for
further details.
