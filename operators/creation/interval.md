# interval

#### signature: `interval(period: number, scheduler: Scheduler): Observable`

## Emit numbers in sequence based on provided timeframe.

<div class="ua-ad"><a href="https://ultimateangular.com/?ref=76683_kee7y7vk"><img src="https://ultimateangular.com/assets/img/banners/ua-leader.svg"></a></div>

### Examples

##### Example 1: Emit sequence of values at 1 second interval

( [jsBin](http://jsbin.com/vigohomabo/1/edit?js,console) |
[jsFiddle](https://jsfiddle.net/btroncone/x3mrwzr0/) )

```js
import { interval } from 'rxjs/observable/interval';

//emit value in sequence every 1 second
const source = interval(1000);
//output: 0,1,2,3,4,5....
const subscribe = source.subscribe(val => console.log(val));
```

### Additional Resources

* [interval](http://reactivex.io/rxjs/class/es6/Observable.js~Observable.html#static-method-interval)
  :newspaper: - Official docs
* [Creation operators: interval and timer](https://egghead.io/lessons/rxjs-creation-operators-interval-and-timer?course=rxjs-beyond-the-basics-creating-observables-from-scratch)
  :video_camera: :dollar: - André Staltz

---

> :file_folder: Source Code:
> [https://github.com/ReactiveX/rxjs/blob/master/src/internal/observable/interval.ts](https://github.com/ReactiveX/rxjs/blob/master/src/internal/observable/interval.ts)
