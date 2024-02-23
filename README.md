[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/P3kz0bBR)
# BEM in practice

## Example 1
    <header class="card card__header">
        <h2 class="card card__h2">Cars</h2>
        <h3 class="card card__h3">Fiat</h3>
        <h3 class="card card__h3">Opel</h3>
        <h3 class="card card__h3">Volvo</h3>
    </header>

#### Solution 1:
    <header class="card__header">
        <h2 class="card__header--title">Cars</h2>
        <h3 class="card__header--subtitle">Fiat</h3>
        <h3 class="card__header--subtitle">Opel</h3>
        <h3 class="card__header--subtitle">Volvo</h3>
    </header>
> [!NOTE]
> block: card, element: header, modifier: title/subtitle

#### Solution 2:
    <header class="card__header">
        <h2 class="card__header card__header--title">Cars</h2>
        <h3 class="card__header card__header--subtitle">Fiat</h3>
        <h3 class="card__header card__header--subtitle">Opel</h3>
        <h3 class="card__header card__header--subtitle">Volvo</h3>
    </header>
> [!NOTE]
> this solution can be correct in case class `card_header` consist of some styles that cannot be inherit and needed to be specified and are shared between all headers

## Example 2
    .card__dog {
        background-color: pink;
    }
    
    .card__cat {
        background-color: yellow;
    }

## Example 3
    .new-card {
      border: solid 1px rgb(255, 242, 0);
      border-width: 2rem;
      max-width: 260px;
      padding: 10px;
      }

## Example 4
    <p class="card__description--text">
        Lorem ipsum dolor...
    </p>

## Example 5
> [!TIP]
> What is a purpose of section? does it make sense to call it "card"?

> [!TIP]
> There are more mistakes to fix here :)

    <section class="card">
        <article class="card__article--dog">
            <aside class="article__do--aside">
                <figure class="article__dog--figure">
                    <img src="..." alt="dummy-image" class="image" />
                </figure>
             </aside>
         </article>
    </section>

## Example 6
    .button__styled--disabled{
        background-color: orange;
    }

## Example 7
    <article class="card__cat">
      ...
    </article>

## Example 8
    <article class="card--dog--type1">
      ...
    </article>

## Example 9
    .card {
        background-color: white;
        margin-bottom: 20px;
        padding: 15px;
        display: block;
        align-items: center;
        justify-content: center;
        border: solid 1px #000;
        max-width: 360px;
        padding: 20px;
    }

## Example 10
    .card__header--dog--type1{
        background-color: green;
    }

    .card__header--dog--type2{
        background-color: purple;
    }

    .card__header--dog--type3{
        background-color: orange;
    }

## Example 11
    <main>
        ...
    </main>
> [!TIP]
> Why is it not a good idea to specify type of flex applied to element in the name of class?

    
## Example 12
    <section class="card__section--dog">
        ...
    </section>

// Add this to css instead //
    card__section--dog {
        show: flex;
    }

## Example 13
    <footer class="card__options">
      <div class="card__options--buttons">
       ...
      </div>
    </footer>

## Example 14
    <header class="card__header--dog">
        <h2 class="card__header--subtitle">Dog Poster</h2>
        <h3 class="card__header--subtitle">Dog poster - 50nok</h3>
    </header>

## Example 15
    <header class="card__header">
        <h2 class="card__cat--title">NEW! Cat Poster</h2>
        <h3 class="card__cat--subtitle">Cat poster - 50nok</h3>
    </header>

## Example 16
    <section class="card__section--cat">
        ...
    </section>

## Example 17
    <button class="card__basked-button--styled-disabled">
        <span class="card__basket-button--icon">&#128722;</span>
        <span class="card__basket-button--text">Basket</span>
    </button>

## Example 18
    <header class="main__header">
        <h1>BEM</h1>
        <button class="button__styled--disabled--wishlist">
            <span>🚀</span>
            <span>Wish list</span>
        </button>
    </header>
    </header>

    <main class="main">
        <section>
        <section>
    </main>

## Example 19
> [!TIP]
> Why it is not a good idea to style cards based on `nth-of-type(even)` in context of shopping cards?
> In which context it will be a good idea?

    .card, .card__basked-button {
        ...
    }

## Example 20
> [!TIP]
> Why it is not a good idea to create repetitive styles based on id?
> In which context we should use ids?

    #wishlist {
        ...
    }

    Because to keep the code clean and not "DRY" you should only use id when there is only 
    one thing that has that same style, i there are multiple then use classes

## Example 21
    <main>
        ...
    </main>

## Example 22
> [!TIP]
> BEM stands for block__element--modifier, is "cat" and "dog" an element? 

    <section class="card__section--cats">
        ...
    </section>

    Cat would be a modifier.

## Example 23
> [!TIP]
> Let's assume that in some case it make sense to call a section "cat" or "dog", the section "cat" will consist of multiple cards of cats, and the section "dog" will consist of multiple cards of dogs. Let's not focuse here on BEM. Nevertheless, how could you improve on class naming?
> 

    <section class="card__cat">
        ...
    </section>

## Example 24
    .button__div1,
    .button__div2 {
        display: flex;
        flex-direction: row-reverse;
    }

    Without more context this coulb be right if there is more indivual styles for div2, 
    if not it would be resonable to name the divs just div instead of having 2 

## Example 25
![image](https://github.com/aniWeyn/advancedcss-bemmistakes/assets/23743322/57049158-a239-4853-aa76-c2cf63e443fe)

The ".card_content > p {}" should be beneath the comment that specifies card selectors.

## Example 26
    header {
      background-color: hsl(180, 31%, 95%);
      ...
    }

    header > button {
      border: none;
      ...
    }

    header > button:hover {
       background-color: hsl(180, 25%, 73%);
    }

    header > button:active {
      background-color: hsl(180, 29%, 50%);
    }

    Maybe add spaces unless i am unsure

## Example 27
In what scenarios is it advantageous to use a class name that represents the animal, and in what scenarios would it be preferable to use a generic name like 'product_01' or 'product_02'?

If you have a wide range of different products (and those products aren't all about animals) you probably shouldn't name each and every one of them with a different animal name. If the product you're selling handles specifically about animals, then in that context it would be acceptable.
