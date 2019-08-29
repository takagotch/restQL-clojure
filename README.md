### restql-clojure
---
https://github.com/B2W-BIT/restQL-clojure

```cljc
// src/main/restql/core/validator/core.cljc

(ns restql.core.validator.core
  (:require [restql.core.validator.util :refer [default rule]]
    [restql.core.encoders.core :as encoders]
    [clojure.set :as s]
    [restql.core.query :as query]
  #?(:clj (:use [slingshot.slingshot :only [try+]])
     :cljs (:use [goog.Uri :only [parse]]))))

(defn without-from [[_ data]]
  (not (contains? data :from)))

(defn invalida-data-key [key]
  (not
    (#(:from :in :method :with :with-headers :with-body :timeout :select) key)))
    
(defn keyword-or-vector? [value]
  (or
    (keyword? value)
    (vector? value)))




```

```
```

```
```


