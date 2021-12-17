# Android Architect  PaperKit
how to become Android Architect? 
how to become a multi-platform Architect? 

## Basic Rules
- if you have a plan to use KMM, select a kmm library from beginning 
- team and time, Reactive programming is a good tool with a high learning curve when time is limited and the team is not confirmable take the next tool
- android has a lot of libaray , try to select a libary that works with xml/compose in future you have to remove xml 
- do not change your tool for the legacy projects, mixing is not good , until you have a very very good plan

_these tools only recommendation not take things personal_

# Good news 
- kmm support 100% code sharing android/ios for business logic
- Compose reach android/desktop/web , soon we will have another flutter wrriten in kotlin

## Architecture Patterns
    MVC : leave the interview because this company retarded
    MVP : dead why? each screen required two interfaces (presenter/view), mocking for test...
    MVVM : always 
    UDF : try to use udf pattern to simplify MVVM 
    MVI : alterantive to mvvm/udf
   
## Dependency injection 
    Manual: using kolin (lazy , Default Values )
    koin: easy swipe Imp.
    dagger hilt: good tool until testing
    
## Reactive Programming:
    Flows API  
    Channels: use Flows API to be consistent 
    reaktive : good library for Reactive Programming multi-platform
    RXJava : avoid RXJava , almost dead  
    rxbinding :android xml views to streams
    
## API Flows
    StateFlow: state holer
    shardFlow: one time event
    turbine : libaray for flow testing

## DateBase
    Room db : always
    SQLite/cipher : use can close Roomdb with password 
    SQLDelight (kmm)
         
## HttpClient
    Retrofit2 : always , al lot of support
    ktor(kmm)
        
## Json Pasring 
    Gson
    kotlinx.serialization(kmm)
    mosi
    
## UI
    Compose (avoid XML as you can)
    material3: something changes button color as wallpaper, do not need it
    
## State Presnenatiton 
    xml : liveData,StateFlow(use it always for consistent)
    compose : StateFlow
    runtime.State : compose

## imagepicker
    dhaval2404: camera/gallery/Image croping
   
## Image Loader
    Coil : always (compose/xml)
    Picasso
    Glide
    
## Archituect Component
    Navigation Component
    Data Binding: I am using compose
    WorkManager: any BG task, or tasks cannot be canceled like (Twitter post)
    DateStore :  handles data migration, guarantees data consistency, and handles data corruption
    shared-preferences : will be replaced with DateStore 
    Live data
    pagging3 : avoid this library, build your paging system , a lot of functionality is missing
     
## Testing 
    Truth : google assertion library, assertions are made with chained method calls,
    Hamcrest : more power than Truth but more complex
    Espresso : android UI test
    Mokitio : never because java is outdated 
    mockK : always
    Robolectric : android test run as local test
    kover:kotlin test coverage
    
## Authutication
    Firebase 
    Auth0

## Payment 
    Stripe

## Kotlin Multiplatform Mobile
    SQLDelight
    Ktor
    kotlinx.serialization
    kotlinx-datetime
        
## static analysis (add this to CI pipeline)
    ktlint : code fromater and checker, make  sure to 
    Detekt: checks for code smells. Examples include magic numbers, complicated conditionals, long methods  
     
## Automation 
    triplet.play , CD pipeline tools , push apks to playStore
    openapi.generator , yaml files to kotlin data class 
    Dangerfile : automated PR review, writing comments on pr like(
    Please add labels to this PR. , Please consider breaking up this pull request. Please provide a summary in the Pull Request description)
    
## Branching strategy 
    gitflow : complex, a lot of conflicts , complex
    Truck-base : short live branches with minimum conflicts, google use this approach
