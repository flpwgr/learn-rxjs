# timer

#### signature: `timer(initialDelay: number | Date, period: number, scheduler: Scheduler): Observable`

## After given duration, emit numbers in sequence every specified duration.

<div class="ua-ad"><a href="https://ultimateangular.com/?ref=76683_kee7y7vk"><img src="https://ultimateangular.com/assets/img/banners/ua-leader.svg"></a></div>

### Examples

##### Example 1: timer emits 1 value then completes

( [jsBin](http://jsbin.com/pazajanehu/1/edit?js,console) |
[jsFiddle](https://jsfiddle.net/btroncone/vpx0y8fu/) )

```js
import { timer } from 'rxjs/observable/timer';

//emit 0 after 1 second then complete, since no second argument is supplied
const source = timer(1000);
//output: 0
const subscribe = source.subscribe(val => console.log(val));
```

##### Example 2: timer emits after 1 second, then every 2 seconds

( [jsBin](http://jsbin.com/kejidofuje/1/edit?js,console) |
[jsFiddle](https://jsfiddle.net/btroncone/30ddov8j/) )

```js
import { timer } from 'rxjs/observable/timer';

/*
  timer takes a second argument, how often to emit subsequent values
  in this case we will emit first value after 1 second and subsequent
  values every 2 seconds after
*/
const source = timer(1000, 2000);
//output: 0,1,2,3,4,5......
const subscribe = source.subscribe(val => console.log(val));
```

### Related Recipes

* [HTTP Polling](../../recipes/http-polling.md)


### Additional Resources

* [timer](http://reactivex.io/rxjs/class/es6/Observable.js~Observable.html#static-method-timer)
  :newspaper: - Official docs
* [Creation operators: interval and timer](https://egghead.io/lessons/rxjs-creation-operators-interval-and-timer?course=rxjs-beyond-the-basics-creating-observables-from-scratch)
  :video_camera: :dollar: - André Staltz

---

> :file_folder: Source Code:
> [https://github.com/ReactiveX/rxjs/blob/master/src/internal/observable/timer.ts](https://github.com/ReactiveX/rxjs/blob/master/src/internal/observable/timer.ts)
