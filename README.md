# named-entity

A Clojure library for named entity extraction.

*IN PROGRESS*

## Usage

```clojure
(ns my-ns
  (:require [named-entity.core :refer all]))

;; Extract entities of a given type (person, location, date or time)

(extract-entities :person "I spoke to Jack Dorsey at the weekend")
;; [{:token "person", :value "Jack Dorsey"}]

;; Extract all entities (slower)

(extract-entities "Working with David in London Tomorrow afternoon at 6pm")

;; {:token "person", :value "David"}
;; {:token "date", :value "Tomorrow"}
;; {:token "time", :value "afternoon"}
;; {:token "location", :value "London"})

```

## License

Copyright © 2014 Owain Lewis

Distributed under the Eclipse Public License either version 1.0 or (at
your option) any later version.
