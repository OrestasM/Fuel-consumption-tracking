# Gasolic
## Description
- [ ] The main purpose for this WEB system is individual vehicle fuel-consumption tracking.

## Entity definition
- [ ] The main entity of this WEB system is a vehicle.
- [ ] Vehicle entity does not have name, but it can be identified by its license plate.
- [ ] Entity has these attributes:
    - [ ] ID – String, created by MongoDB when inserting entity into database.
        - [ ] No restrictions
    - [ ] Creation date – ISO 8601 date string, which defines when entity was inserted into database.
        - [ ] Joi.date().min(“now”).max(“now”);
    - [ ] Owner ID – Number, ID of user, who owns particular vehicle.
        - [ ] No restrictions
    - [ ] Current mileage – Number, which defines current vehicle mileage.
        - [ ] Joi.number().min(0).max(10000000);
    - [ ] Engine capacity – Number, which defines vehicle engine capacity.
        - [ ] Joi.number().min(0).max(20000);
    - [ ] Year of make – Number, which defines in which year vehicle was made.
        - [ ] Joi.number().min(1900).max(2019);
    - [ ] Make – String, which defines the vehicle make.
        - [ ] Joi.string().max(30);
    - [ ] Model – String, which defines the vehicle model.
        - [ ] Joi.string().max(30);
    - [ ] License plate – String, which defines vehicle’s license plates.
        - [ ] Joi.string().max(30);

## API definition
- [ ] The main thing this WEB system will get from API is all makes and models of vehicles.
- [ ] API has these methods (used in this WEB system):
    - [ ] Get makes
        - [ ] (GET) https://www.carqueryapi.com/api/0.3/?callback=?&cmd=getMakes
    - [ ] Get models
        - [ ] (GET) https://www.carqueryapi.com/api/0.3/?callback=?&cmd=getModels&make={make}
## UI definition
[Add new vehicle UI](https://farm8.staticflickr.com/7873/47488118431_88bdd06d22_b.jpg)
    - This UI allows user to add a new vehicle on its vehicle list.

[Control your vehicles UI](https://farm8.staticflickr.com/7920/40522194383_cc7990f0d3_z.jpg)
    - This UI allows user to control already added vehicles - add their consumption, see various graphs of fuel consumptions, etc.
