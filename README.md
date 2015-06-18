# Cards
Sass card snippet for making css and html cards.

Card is covered by a div when hovering it.
The card can have heading, body, footer, etc.
Depending on where the cover div is put it will roll up and down to show addtional content when hover the card div.

# Usage
HTML

<div class="card">
  <div class="card__heading">
    <h3>Lorem ipsum dolor sit amet.</h3>
    <p class="noticia__info">Medio - 05/12/2015</p>
  </div>

  <div class="card__body">
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sint, ab non nobis laborum architecto</p>
    <div class="card__cover">
      <p >Read more...</p>
    </div>
  </div>
  <div class="card__footer clearfix">
    <p>Footer text.</p>
  </div>
</div><!-- ./card -->


SCSS

/*--------------------------------*\
  CARDS
\*--------------------------------*/

.card,
%card{
  width: 300px;
  outline: 1px solid #ccc;
  position: relative;
  overflow: hidden;
  & > *{
    position: relative;
    overflow: hidden;
  }
  &:hover{
    & .card__cover{
      top: 0;
      
    }
  }
}

  .card__heading{
    //outline: 1px solid #ccc;
  }

  .card__body{
    //outline: 1px solid #ccc;
  }

  .card__footer{
    //outline: 1px solid #ccc;
  }

.card__cover{
  background-color: #ccc;
  position: absolute;
  top: 100%;
  left: 0;
  width: 100%;
  height: 100%;
  transition: top 0.2s ease;
}
/*--------------------------------*\
  ./CARD
\*--------------------------------*/
