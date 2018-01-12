# How you Test ngRx
  This repository is for testing of effects, actions, reducers.
  
## Getting Started

These instructions will get you some samples of the project up. Basically You DON'T need to use TestBed with those test cases.
Please read https://github.com/vsavkin/testing_ngrx_effects. It's some recommandactions for testing effects.

### Prerequisites
What environment I am using:
    "@ngrx/store": "^4.1.0"
    "jasmine-core": "~2.6.2",
    "@nrwl/nx": "0.5.1",
    and Angular 5
What things you need to know 

     https://github.com/vsavkin/testing_ngrx_effects testing NgRx Effects without TestBed
     https://github.com/ReactiveX/rxjs/blob/master/doc/writing-marble-tests.md for hot, cold observable
     https://github.com/ngrx/platform/blob/master/docs/effects/testing.md for testing metadata


### Installing


```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Testing Effects

  
   *  Notice: Testing for Effects should create stub services for all inject service `without` TestBed
     
     Steps:
       1. create first action
       2. make it a new actions which return a observable
       3. create expected action
       4. make expected action to another observable
       5. create effrects service with stub service and action
       6. check the specific effect return the same structure obsersable
   
     There are two parts you should test
       1. check the effects return a right action that you expected
       2. check the effects return a wrong action that you expected
       3. the metadata of an effect (dispatch attribute: true or not)

## Testing with Actions

  *  Notice: Testing Actions `without` TestBed

    Steps:
       1. Create the action
       2. Check type and payload of actions equal to the action you created
  For Example:
       
       const action = new fromUsers.LoadUser();
       expect({ ...action }).toEqual({ type: fromUsers.LOAD_USER });

## Testing with Reducers

   *  Notice: Testing for reducers without TestBed

    Steps:
          1. create action with parameter if needs and call reduce function with initial state and action
          2. check values in state are right after action dispatched




# Keep Updating Example later on
