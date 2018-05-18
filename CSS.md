### GRID-LAYOUT

1. Medida fr
es una medida totalmente responsive, ya que ocupa la fracción de espacio restante. Es decir, si ponemos varias columnas con medida .rem y una columna con medida 1fr, las primeras mantendrán la medida e la otra se expandirá hasta ocupar el espacio restante

2. Si nuestro grid puede crecer en el futuro porque probablemente agreguemos nuevas filas con itens por debajo, substituiremos grid-template-rows por grid-auto-rows (en este caso no tiene sentido colocar un número de rows ya que sse irán gerenando automáticamente a medida que agreguemos filas):
```CSS
   .tasks-wrapper{
        display: grid;
        grid-template-columns: [leftGap] 2rem [centCol] 1fr [rigthGap] 2rem;
        grid-auto-rows:  1.3rem
        grid-row-gap: .3rem;
      }
```

```Gráfico
       row  ⬜️ 
       row  ⬜️       
       row  ⬜️ ⬇
```




### TIPS CSS

* seleccionar elementos pares e impares:

```CSS
.grid-item{
    padding: 1.5rem
}
.grid-item:nth-child(2n){
    background-color: black
}
.grid-item:nth-child(2n+1){
    background-color: white
}
```

* hacer que las imágenes sean responsive:

```CSS
// max-width:100% hace que la imagen respete su contenedor y no crezca más que el tamaño del contendor, sobresaliendo

img{
    max-width:100%;
    height:auto;
}
```

* crear un background transparente:

```CSS
background: rgba(54, 25, 25, .00004);
```


 