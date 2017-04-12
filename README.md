# knowledge-transfer

## Angular intro - Create simple 'html template driven' web form
##### Demo2 illustrates creating a web form and storing the values in a model class

- Go back to [lesson 1](https://github.com/sardeenz/demo3).

### High Level Overview
- create user model
- add html form to the user component's template
- make the form pretty with a global stylesheet

#### 1. Create user model
   * `ng g class user` (creates user.ts - this is your user form model)
   * create form variables in user.ts
   * bind the html form fields to the user.ts model.

#### 1. Add html for the form
   ~~~~
<div class="app-content">
    <h1>Inside Customer Form</h1>
    <form (ngSubmit)="onSubmit()" class="ui form">
        <md-card class="app-input-section">
            <div class="form-group">
                <label for="firstname">First Name</label>
                <input type="text" class="form-control" id="firstname" required [(ngModel)]="form.firstname" name="firstname"> TODO: remove this: {{form | json}}
            </div>
            <div class="form-group">
                <label for="lastname">Last Name</label>
                <input type="text" class="form-control" id="lastname" required [(ngModel)]="form.lastname" name="lastname">
            </div>
            <button md-button type="submit" class="btn btn-success">Submit</button>
        </md-card>
    </form>
    <div>
        {{users | json}}
    </div>
</div>
~~~~

#### 3. Make it look pretty
   * add this to styles.css (global stylesheet)
   * `@import 'https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css';`

#### 5. Proceed to [lesson 3](https://github.com/sardeenz/demo3)

- tips