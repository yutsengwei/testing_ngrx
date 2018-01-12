# How you Test ngRx

  1. effects
  2. actions
  3. reducers
  
  <br>

# Testing Effects

  
   *  Notice: Testing for Effects should create stub services for all inject service without TestBed
      Take a look with
     https://github.com/vsavkin/testing_ngrx_effects testing NgRx Effects without TestBed
     https://github.com/ReactiveX/rxjs/blob/master/doc/writing-marble-tests.md for hot, cold observable
     https://github.com/ngrx/platform/blob/master/docs/effects/testing.md for testing metadata
     Steps:
       1. `create first action`
       2. `make it a new actions which return a observable`
       3. `create expected action`
       4. `make expected action to another observable`
       5. `create effrects service with stub service and action`
       6. `check the specific effect return the same structure obsersable`
   
     There are two parts you should test
       1. `check the effects return a right action that you expected`
       2. `check the effects return a wrong action that you expected`
       3. `the metadata of an effect (dispatch attribute: true or not)`
   
