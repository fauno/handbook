Compartir archivos
==================

El término *compartir archivos* se refiere a la práctica de compartir archivos en la red, a menudo con la distribución más amplia posible en mente. Desafortunadamente en los últimos años se ha asociado popularmente con la distribución de contenido registrado bajo ciertas licencias de derechos de autor que no permiten la distribución de copias (por ejemplo supuesta actividad criminal). A pesar de esta nueva asociación, el intercambio de archivos sigue siendo una herramienta vital para todo el mundo: desde grupos académicos a las redes científicas y las comunidades de software libre.

En este libro intentamos ayudarlo a que aprenda a distribuir archivos en forma privada, con el consentimiento de algunas personas, sin que otras puedan acceder al contenido que intercambia ni que la transacción sea interceptada. Usted está protegido por su derecho básico al anonimato y a no ser espiado. La sospecha de que los contenidos podrían haber sido robados y no ser suyos no es  razón suficiente para socavar su derecho a la privacidad. 

La historia de Internet está plagada de ataques de diferentes tipos de nodos de publicación y distribución, realizadas por diferentes medios (orden judicial, ataques de denegación de servicio). Lo que este tipo de eventos han demostrado es que si uno quiere que la información esté disponible en forma persistente y resistente contra los ataques, es un error confiar en la neutralización de un único nodo.

Esto ha sido demostrado recientemente por la clausura del servicio de descarga directa Megaupload, cuya desaparición provocó la pérdida de grandes cantidades de datos de sus usuarios, en gran parte ajeno incluso a las supuestas infracciones de copyright que sirvieron de pretexto para su cierre. En la misma línea los ISPs suelen acabar con los sitios web que contengan material dudoso simplemente porque les resulta más barato hacerlo que acudir a los tribunales y que un juez decida. Estas políticas dejan la puerta abierta a la intimidación por parte de todo tipo de empresas, organizaciones e individuos listos y dispuestos a hacer un uso agresivo de cartas legales. Tanto los servicios de descarga directa como los ISP son ejemplos de estructuras centralizadas que no pueden ser invocados porque son puntos débiles para el ataque, y debido a que sus intereses comerciales no están alineados con los de sus usuarios.

Difundir a través de los archivos de distribución, la descentralización de los datos, es la mejor manera de defenderse contra estos ataques. En la siguiente sección dos ámbitos de intercambio de archivos se perfilan. El primero son las tecnologías estándar de p2p cuya técnica de diseño está determinado por la eficiencia de las redes para permitir la velocidad de distribución y descubrimiento de contenido a través de mecanismos de búsqueda asociados. El segundo se centra en I2P como un ejemplo de una darknet llamada, su diseño da prioridad a la seguridad y el anonimato durante otros criterios que ofrecen una robusta, aunque menos eficiente de los recursos, ruta de acceso a la disponibilidad persistente.

Los medios de compartir archivos mencionados a continuación son sólo algunos ejemplos de las muchas tecnologías P2P que se han desarrollado desde 1999. BitTorrent y Soulseek tienen enfoques muy diferentes, sin embargo ambos fueron diseñados para la facilidad de uso por un público amplio y tienen importantes comunidades de usuarios. I2P, de más reciente desarrollo, tiene una base de usuarios pequeña.

**BitTorrent** se ha convertido en el sistema P2P para compartir archivos más popular. La controversia que lo rodea hoy en día irónicamente ha ayudado a la comunidad a crecer, mientras que la policía, impulsada por los poderosos dueños de los derechos de autor, aprovechan los registros de los servidores para perseguir a sus operadores, a veces hasta el punto de encarcelarlos como en el caso de The Pirate Bay.

**Soulseek** - si bien nunca ha sido la más popular entre las plataformas de intercambio de archivos, tampoco ese es su objetivo. Soulseek se centra en el intercambio de música entre los simpatizantes, productores independientes, aficionados e investigadores. El sistema y la comunidad que lo rodea está completamente aislada de la web: no hay enlaces externos a los archivos de Soulseek. Estos archivos se mantienen exclusivamente en los discos duros de sus usuarios. El contenido de la red depende totalmente de cuántos miembros están conectados y cuántos lo comparten. Los archivos se transfieren sólo entre dos usuarios a la vez y nadie más que esos dos usuarios se involucran. Debido a esta "introvertido" carácter - y la especificidad de su contenido - Soulseek se ha mantenido fuera de la vista de los defensores de los derechos de autor y la legislación anticopia.

**I2P** es uno de varios sistemas desarrollados para resistir la censura (otros incluyen FreeNet y Tor) y cuenta con una comunidad de usuarios mucho menor, se destaca aquí por su inclusión de la funcionalidad de Bit Torrent en su instalación básica. Estos sistemas también pueden ser utilizados para proporcionar servicios ocultos, entre otros, lo que le permite publicar páginas Web en sus entornos..

BitTorrent
----------

BitTorrent es protocolo P2P que facilita la distribución de los datos almacenados en varios nodos / participantes de la red. No hay servidores centrales o concentradores, cada nodo es capaz de intercambiar datos con cualquier otro nodo, a veces cientos de ellos al mismo tiempo. El hecho de que los datos se intercambian en partes entre numerosos nodos permite grandes velocidades de descarga de los contenidos más populares en las redes BitTorrent, por lo que se ha convertido rápidamente en el estándar de facto entre las plataformas de intercambio de archivos P2P.

Si utiliza BitTorrent para distribuir material de dudosa legalidad, usted debe saber que las fuerzas de seguridad habitualmente recopilan información sobre presuntos infractores participando en enjambres torrent, observando y documentando el comportamiento de los otros pares. El gran número de usuarios en constante aumento crea un problema para aplicar este sistema - simplemente no tienen recursos suficientes para perseguir a todos los usuarios. Cualquier caso judicial requerirá evidencia real de transferencia de datos entre el cliente y otro par (y por lo general la evidencia de  la carga del archivo); sin embargo, es suficiente que usted proporciona una parte del archivo, no el archivo en su totalidad, para ser acusado. Si usted prefiere ser mas precavido, debe utilizar una VPN para enrutar el tráfico de BitTorrent, como se detalla en el capítulo **Uso de VPN**.

La descarga de un archivo de la red BitTorrent comienza con un archivo torrent o con un enlace magnet. Un archivo torrent es un archivo pequeño que contiene información sobre los archivos de mayor tamaño que desea descargar. El archivo torrent le dice a su cliente de torrent los nombres de los archivos que se comparten, una dirección URL para el seguidor y un código hash, que es un código único derivado del archivo subyacente al cual representa - algo así como una identificación o número de catálogo. El cliente puede utilizar el hash para encontrar la semillas de otros (para subir) esos archivos, así puede descargar desde su computadora y comprobar la autenticidad de los fragmentos a medida que llegan.

Un *enlace magnet* elimina la necesidad de un archivo torrent y es esencialmente un hipervínculo que contiene una descripción de ese torrent que su cliente puede usar inmediatamente para empezar a buscar personas que compartan el fichero que está dispuesto a descargar. Los enlaces magnet no requieren de un tracker, sino que dependen de la *tabla hash distribuidas (DHT)* - se puede leer más en el Glosario – y en *Mecanismo de intercambio*. Los enlaces magnet no hacen referencia a un archivo por su ubicación (por ejemplo, mediante las direcciones IP de las personas que tienen el archivo o URL) sino que definen los parámetros de búsqueda que permiten encontrar el archivo. Cuando se carga un enlace magnet, el cliente torrent inicia una búsqueda de disponibilidad que se transmite a otros nodos y es básicamente una nota -"¿quién tiene algo que coincida con el hash?". El cliente torrent se conecta a los nodos que respondieron a la nota de salida y comienza a descargar el archivo.

BitTorrent utiliza cifrado para evitar que los proveedores y otros man-in-the-middle bloqueen o espíen el tráfico basándose en el contenido que usted intercambia. Ya que los enjambres de BitTorrent (rebaños de semillas y leechers) son libres para que todo el mundo pueda unirse a ellos es posible que alguien lo haga y recopile información acerca de todos los pares conectados. El uso de enlaces magnet no evitará que lo detecten entre la multitud, ya que todos los nodos que comparten el mismo archivo deben comunicarse entre sí -y, por tanto, aunque sólo uno de los nodos del enjambre sea un tramposo, será capaz de ver su dirección IP. También será capaz de determinar si usted está sembrando los datos mediante el envío de su nodo de una solicitud de descarga.

Un aspecto importante del uso de BitTorrent es digno de una mención especial. Cada fragmento de datos que recibe (leecher) está siendo compartida instantáneamente (sin semillas) con otros usuarios de BitTorrent. Por lo tanto, un proceso de descarga se transforma en un proceso (involuntario) de publicación, utilizando un término legal pone a disposición los datos, antes de que la descarga se complete. Mientras BitTorrent se utiliza a menudo para volver a distribuir el software libremente disponible y legítimo, películas, música y otros materiales, su capacidad de "puesta a disposición" ha creado mucha controversia y dio lugar a un sinfín de batallas legales entre los titulares de derechos de autor y los facilitadores de plataformas BitTorrent. En el momento de escribir este texto, el co-fundador de The Pirate Bay Gottfrid Svartholm se encuentra detenido por la policía sueca tras una orden internacional dictada contra él.

Por estas razones, y por las campañas de relaciones públicas de los titulares de los derechos de autor, el uso de las plataformas de BitTorrent se ha convertido prácticamente en sinónimo de piratería. Y aunque todavía no está claro el significado de términos como piratería, derechos de autor y propiedad en el contexto digital, muchos usuarios comunes de BitTorrent han sido perseguidos acusados de violar las leyes de derechos de autor.

La mayoría de los clientes torrent le permiten bloquear direcciones IP de los trolls conocidos de derechos de autor usando listas negras. En lugar de usar torrents públicos también se puede unir a trackers de BitTorrent cerrados o utilizarlos a través de VPN o Tor. 

En las situaciones en las que usted cree que debería estar preocupado por el tráfico de BitTorrent y su anonimato debería verificar lo siguiente:

 * Compruebe si su cliente soporta listas negras de pares. 
 * Compruebe si las definiciones de las listas negras de pares se actualizan diariamente. 
 * Asegúrese que su cliente soporte la totalidad de los protocolos más recientes - DHT, PEX y enlaces Magnet. 
 * Elija un cliente torrent que soporte cifrado de pares y habilítelo. 
 * Actualice o cambie su cliente torrent si algo de lo mencionado más arriba no está disponible. 
 * Use una conexión VPN para ocultarle su tráfico BitTorrent a su ISP. Asegúrese que su proveedor de VPN permite el tráfico P2P. Vea más consejos y recomendaciones en el capítulo Uso de VPN. 
 * No siembre ni guarde semillas si no sabe mucho acerca de ello. 
 * Sospeche de los enlaces muy populares o con comentarios muy positivos. 
 * Verifique si su cliente torrent soporta listas negras de pares.
 
SoulSeek
--------

Como en el caso de los programas para compartir archivos entre pares (P2P), los usuarios de Soulseek determinan el contenido disponible, y cuáles archivos se pueden compartir. La red tuvo históricamente una mezcla de música diversa, incluyendo artistas independientes y alternativos, música inédita, tales como demos y cintas de las mezclas, grabaciones piratas, etc. Está totalmente financiado por donaciones, sin publicidad ni cobro de tarifas a usuarios.

> Soulseek no avala ni aprueba el intercambio de materiales con copyright. Sólo debe compartir y descargar archivos para los cuales usted está legalmente autorizado, o ha recibido permiso." (consulte su [página web](http://www.soulseekqt.net))

La red de Soulseek depende de un par de servidores centrales. Uno soporta al cliente original y a la red, y el otro soporta a la red más nueva. Mientras que estos servidores centrales son claves para coordinar búsquedas y hospedar salas de chat, no juegan ningún rol en la transferencia de archivos entre usuarios, que se desarrolla directamente entre ellos.

Los usuarios pueden buscar por ítem, los resultados devueltos serán una lista de los archivos cuyos nombres coinciden con el término de búsqueda utilizado. Las búsquedas pueden ser explícitas o pueden utilizar comodines/patrones o condiciones para ser excluidos. Una característica específica al motor de búsqueda Soulseek es la inclusión de los nombres de las carpetas y las rutas de archivo en la lista de búsqueda. Esto permite a los usuarios buscar por nombre de carpeta.

La lista de resultados de búsqueda muestra los detalles, como el nombre completo y la ruta del archivo, su tamaño, el usuario que aloja el archivo, junto con la tasa promedio de transferencia  de los usuarios y, en el caso de archivos mp3, detalles breves acerca de la pista codificada en sí, tales como la velocidad de bits, longitud, etc. La lista de búsqueda resultante puede entonces ser ordenada en una variedad de formas y archivos individuales (o carpetas) seleccionados para su descarga.

A diferencia de BitTorrent, Soulseek no es compatible con la descarga desde fuentes múltiples o "swarming" como otros clientes post-Napster, y deben buscar un archivo solicitado desde una sola fuente.

Si bien el software Soulseek es libre, existe un sistema de donación para apoyar el esfuerzo de programación y el costo de mantenimiento de los servidores. A cambio de donaciones, a los usuarios se les concede el privilegio de ser estar por delante de los usuarios que no hagan donaciones en una cola de descarga de archivos (pero sólo si los archivos no se comparten en una red de área local). Los algoritmos del protocolo de búsqueda Soulseek no se publican, ya que esos algoritmos se ejecutan en el servidor. Sin embargo, existen muchas implementaciones libres de software para clientes y servidores en GNU/Linux, OS X y Windows.

En cuanto a los temas de privacidad y copyright Soulseek está bastante lejos de BitTorrent también. Soulseek ha sido llevado ante los tribunales sólo una vez, en 2008, pero incluso eso no iba a ninguna parte. No hay indicios de usuarios Soulseek que hayan sido llevados ante la corte o acusados de distribución ilegal de material con copyright u otros crímenes del 'milenio digital'.

Si desea usar la red Soulseek con algún grado de anonimato, deberá usarla sobre una VPN.

I2P
---

I2P comenzó como una ramificación del proyecto Freenet, originalmente concebida como un método de publicación y distribución resistente a la censuran. Desde su sitio web:

> El proyecto I2P se formó en el 2003 para apoyar los esfuerzos de aquellos que tratan de construir una sociedad más libre, ofreciéndoles un sistema de comunicación incensurable, anónimo y seguro. I2P es un esfuerzo de desarrollo que produce una red de baja latencia, totalmente distribuida, autónoma, escalable, anónima y resistente. El objetivo es operar con éxito en entornos hostiles - incluso cuando una organización con recursos financieros o políticos lo ataca. Todos los aspectos de la red son de código abierto y están disponibles sin costo, ya que debe asegurar a las personas que lo usan que el software hace lo que dice, al igual que permite que otros puedan contribuir y mejorarlo para derrotar los intentos agresivos que quieren sofocar la libertad de expresión. ([http://www.i2p2.de/](http://www.i2p2.de/))

Para una guía de instalación del software y la configuración de su navegador web consulte la sección sobre Intercambio seguro de archivos - Instalación de I2P. Una vez terminado, el lanzamiento lo llevará a una página de la consola que contiene enlaces a otros sitios y servicios populares. Además de las páginas web habituales (conocidas como eePsites) hay una amplia gama de servicios de aplicaciones disponibles desde la herramienta de blogging para Syndie construido en un cliente de BitTorrent que funciona a través de una interfaz web.




