Find all the countries in region "Asia" :-  db.assg2.find({region:"Asia"})

Find all the countries with currency: "EUR":- db.assg2.find({currency:"EUR"})

Find all the countries whose timezone's gmtOffset is 3600:-  db.assg2.find({"timezones.gmtOffset":3600})

Find all the countries whose timezone's gmtOffset is 3600 AND timezone name is Central European Time (or CET):- db.assg2.find({"timezones.gmtOffset":3600, "timezones.abbreviation":"CET"})

Find All the countries with more than 1 time zone (hint: size of array):-  db.assg2.find({"timezones.1":{"$exists":true}})

Find All the countries with "Korean" translation (KR):- db.assg2.find({"translations.kr":{$exists:true}})