# NLP - The Movie Database (TMDb)

**1. ¿Cómo se pueden categorizar las películas?**

   Según las bases que se tienen se pueden categorizar por:
   
   * Género
   * Compañia de producción
   * País de Producción
   * Fecha de lanzamiento
   * Estado
   * Popularidad
   * Palabras Claves
   
**2. ¿Es posible predecir el éxito de una película dada una cierta combinación de las variables que escogió para la categorización?**

   Si es posible predecir el éxito de una película a partir de la combinacion de las variables que se escogió para la categorización. 
   En este caso se consideró una pelicula exitosa, la cual es rentable. Se considera una pelicula rentable si las ganacias de la pelicula son el doble del costo de la misma. 
   
            movies['profit_per']= round(abs(movies['budget']-movies['revenue'])/movies['budget']*100)
            movies2['success'] = movies2['profit_per'].apply(lambda x: 1 if x > 100 else 0)
            
   A partir de las siguientes variables:
   * popularity
   * vote_average
   * vote_count 
   * gen_bin
   * kword_bin
   * prodCpany_bin
   * cast_bin
   
   Se procedió a utilizar un algorithmo de ML clasificador para la predicción de si una pelicula es exitosa o no.
   
**3. ¿Qué se puede decir de la evolución temporal?**

   A partir de 1990 se puede realizar analisis de la evolución temporal de las películas, dado que en años anteriores se tiene muy pocos datos para sacar una conclusión. Se puede observar lo siguiente:
   
   * De los 26 meses que se estan teniendo encuenta para el analisis, hay 10 meses en el cual se tiene mas peliculas "No Exitosas" que "Existosas". Donde en 1998, 1999, y 2001 se tiene una diferencia entre el 30 y 40 porciento.
   * El año con mayor peliculas exitosas es el 2011, y es el que contiene mayor cantidad de datos en la base.

**4. ¿Qué información útil se puede extraer de los datos?**

   * El país de producción, compañia de producción, y el lenguaje de la pelicula no son muy relevantes para definir si una pélicula es exitosa o no.
   * Al utilizar otros metodos de "word-embedding", es posible que se tengan mejores resultados.
   * 
