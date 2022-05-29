# ⚖️ Injustweet 

_Visibilizando injusticias laborales publicadas en Twitter a través de una plataforma descentralizada basada en blockchain._

## 📚 Sobre el proyecto 

En nuestro día a día, se producen numerosas situaciones de **injusticia** en el **entorno laboral**. Sin embargo, muchas veces, los medios tradicionales de denuncia no son suficiente para visibilizarlas. En los últimos años, con la aparición y expansión de las **redes sociales**, muchas personas han recurrido a ellas para hacerse oír. En particular, Twitter ha jugado un papel muy importante a la hora de visibilizar iniciativas y unir a gente con intereses comunes.

En este contexto, percibimos que, aún significando un avance importante, pueden existir **problemas** si se usan exclusivamente las redes sociales como medio de denuncia. Por ejemplo, la denuncia puede ser censurada por medio de su eliminación, denuncias muy mediáticas pueden eclipsar a otras, o las denuncias pueden quedar ocultas entre la gran cantidad de contenido que hay en la red social. 

Es por ello que proponemos crear una herramienta de **análisis** y **visualización** dedicada, exclusivamente, a este tema. La aplicación **Injustweet**, haciendo uso de estadísticas y gráficas, muestra datos relacionados con denuncias laborales en Twitter. De forma que pueda servir como un punto de **conocimiento**, **apoyo** y **denuncia** para personas que estén interesadas, tanto a nivel personal como profesional, en el tema. 

El desarrollo de la aplicación aprovecha los últimos avances **metodológicos** y **tecnológicos** para llevarla a cabo. Por un lado, el desarrollo del **frontend** se lleva a cabo cuidando el **diseño** gracias a **React**. Por otro lado, con el objetivo de evitar la **censura**, el **backend** hace uso de tecnologías distribuidas, como la **blockchain**. Finalmente, destacamos que con el fin de detectar, entre la gran cantidad de **datos**, aquellas que sean denuncias, se aplican técnicas de análisis de lenguaje natural.

## 🗃 Sobre el repositorio

La arquitectura de la aplicación se divide en tres bloques; el primero recoge datos (tweets) sobre denuncias laborales, otro los almacena de forma distribuida haciendo uso de la blockchain, y un último se encarga de mostrarlos en forma de dashboard en una página web. Todos los repositorios se pueden encuentran en este proyecto. A continuación detallamos cómo están organizados.

### Bloque 1: Recoger datos

- [Previous-work-related-to-data-recollection](https://github.com/injustweet-tfg/Previous-work-related-to-data-recollection)
- [Data-Recollection](https://github.com/injustweet-tfg/Data-Recollection)


### Bloque 2: Guardar datos

- [smart-contract](https://github.com/injustweet-tfg/smart-contract)
- [update-API](https://github.com/injustweet-tfg/update-API)
- [API](https://github.com/injustweet-tfg/API)

### Bloque 3: Mostrar datos

- [cache-twitter](https://github.com/injustweet-tfg/cache-twitter):  Servidor que se encarga de recibir y gestionar peticiones sobre la base de datos de MongoDB.
Esta base de datos actúa como una “memoria caché”. Las llamadas a IPFS son costosas, y además no pueden crearse índices para mejorar la eficiencia, ni tiene un gran variedad de consultas. Por lo tanto, se decide reducir la cantidad de accesos a IPFS a una vez cada dos días, momento en el cuál se actualiza la BBDD que se encarga de proporcionar datos a la aplicación web (“memoria caché”).
- [dashboard-twitter](https://github.com/injustweet-tfg/dashboard-twitter): Representa el frontend de la aplicación. Muestra los datos recogidos en la BBDD que hemos construido.
- [update-cache-twitter](https://github.com/injustweet-tfg/update-cache-twitter): Recoge datos de IPFS cada dos días para actualizar la “memoria caché”.
