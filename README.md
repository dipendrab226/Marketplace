# final-project-pickle-rick
final-project-pickle-rick created by GitHub Classroom
if all the modules installed, docker and redis are running, start backend with pm2 start process.config.js
start front end in the frontend folder with npm start.

# Tech Requirements
- Node back end, Microservice architecture, http, GET, only url, POST, url+body, 
- React Front end, Redux, Redux Thunk, "global state", Use if multiple component share a value, React-router, Websocket
- State/Props, Props, props: passed in, props are read only, state: declared in components, clears any time it mounts
- Storage, redis(cache), key/value storage, pubsub, caching for quick access, store for a certain amount of time, amount of storage, kicks out data on purpose
- Mongodb, nosql, json, kafka(queue), decouples the service that need heavy work from those that don't need the heavy work                                                       

# Devops
- All services run as docker containers                                                  - SOME IN THE DEPLOYMENT BRANCH
- Single docker compose file                                                             - DONE IN DEPLOYMENT BRANCH
- If you get it running on ec2: Extra credit                                                -NO BUT TRIED

# Base architecture requirements
- Assume all services are clusterizable
- User service (auth)                                                                        - DONE
- user collection                                                                            - DONE
- Notification service (real time updates)                                                  - DONE (KIND OF)
- holds ws connections                                                                      - DONE
- alert via redis pubsub                                                                    - DONE

# Transaction service                                                                          - DONE
- Store transactions when user purchases something in mongodb                               - DONE
- who bought it 
- what it was                                                                                - DONE
- how much it was                                                                          - DONE
- Push transaction to kafka queue (offline slow processing)                                  - DONE
- Headed to receipt service                                                                  - DONE
- most of the business logic  
- inventory service                                                                           - DONE
- Has items, prices and inventory                                                             - DONE
- Receipt service                                                                        - DONE
- kafka consumer                                                                           - DONE
- send email to user                                                                      - DONE

# Seller
- Has inventory management                                                                  - DONE
- box to enter an item                                                                      - DONE
- Shows sales
- only their own

# Buyer
- show catalog                                                                               - DONE
- every item from every seller                                                              - DONE
- okay to display if not logged in                                                          - DONE
- Create purchases                                                                          - DONE
- single item                                                                              - DONE
- fancier would be a cart                                                                - DONE
- show purchase history                                                                  - DONE(KIND OF)
- Show item pages                                                                          - DONE

# Items
- item has its own detail page                                                             - DONE
- show how many people are viewing an item (real time)                                     - DONE
- Websocket                                                                                - DONE
- show number of times sold 
- Both
- Display banner notifications when something is purchased (news feed)                    - DONE(KIND OF)
- Synchronize transactions across all tabs                                                - DONE(KIND OF)

