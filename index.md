# LeasingNinja

The LeasingNinja is an example how to use DDDfootnote:[We assume that you are familiar with the DDD nomenclature. If not, you may consider reading XXXX first.]. The idea is to have one domain that is small enough to be grasped easily and big enough to show the different concepts in a real world end-to-end example. There will be different _incarnations_ (i.e. implementations) of the LeasingNinja to show the pros and cons of different styles and solutions. By always using the same domain the details of the various incarnations can be compared easily. Each incarnation is a combination of styles.

We use different styles in: strategic design, implementation of the domain “layer”, programming language and other properties of programming. Strategic stuff contains big ball of mud versus bounded contexts vs CQRS. Domain layer: domain model vs anemic domain model vs polluted domain model vs event sourced domain model. For programming languages we will start with Java and it is planned to eventually add C#, Typescript, Kotlin, PHP, etc.

All incarnations are accessible for everyone under MIT license on GitHub. Some of the better incarnations are meant to serve as blueprint for new projects. The worse incarnations are examples of “how to _not_ do it”. Be warned to use them as blueprints...

## Ok, show me the code!
Not so fast young padawan! The first D in DDD stands for Domain and one important rule is that we have to at least some understanding of the domain before we start coding. (If you want to ignore this warning you can easily jump forward to the incarnations <link>here</link>)

## So, what is the domain in our example?
Imagine Bob wants to reduce his carbon footprint. He likes to change his dirty gas-powered car for a clean new electric car. Unfortunately he doesn’t have a lot of money. But the salesperson at the car dealer says: “No problem: we buy the car for you and rent it to you for a monthly rate (installment).” This is called _leasing_. “Great” says Bob: “How much will it cost me per month?” The salesperson calculates the monthly rate. Bob signs the contract and the salesperson gives the contract into the risk department. There a risk manager looks at Bob’s credit rating and decides that it is good enough. So he votes the contract with “yes”. Only now the contract becomes legally valid. He informs the salesperson and she gives the keys to Bob.

Phew, this is a lot of text!
Let's model it in a more graphical way – a Domain Story.

<Domainstory here>


Now that we gained some understanding of the domain, we can see different bounded contexts.
There is the _Sales_ context and the _Risk Management_ context.

<Context Map here>

Also we can see a lot of words of the domain language.
Verbs like _to sign_ and _to vote_, nouns like _contract_, _monthly rate_ and _credit rating_.
All of them will become parts of our ubiquitous language.