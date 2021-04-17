---
title: Animaciones
description: Animaciones
ms.assetid: 8bd9ac94-3f86-4168-bf33-7a2c8d11907d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf1b9f5e8daa320390f5c19c3c4c27cb8195a8fe
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104560165"
---
# <a name="animations"></a>Animaciones

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Las animaciones de un carácter reflejan el sexo, la edad, la personalidad y el comportamiento. El número y los tipos de animaciones que se crean para un carácter dependen de lo que hace el carácter y de cómo responde a situaciones diferentes.

Al igual que las animaciones tradicionales, las animaciones digitales implican la creación de una serie de imágenes ligeramente diferentes que, cuando se muestran secuencialmente, proporcionan la ilusión de acción. La creación de imágenes de animación de alta calidad puede requerir un animador experimentado, pero el estilo y la presentación del carácter que cree también afectará a la calidad. En ocasiones, los caracteres bidimensionales con formas y características simples pueden ser tan efectivos como (o más efectivos que) los caracteres muy representados. No es necesario crear una imagen realista para describir un carácter efectivo. Muchos caracteres animados populares no son realistas en su presentación, pero son eficaces porque el animador entiende cómo transmitir acciones y emociones. El apéndice proporciona información general acerca de los principios básicos de diseño de animaciones.

### <a name="frames"></a>Imágenes

Cada animación que se crea para un carácter de agente de Microsoft se compone de una secuencia de fotogramas con tiempo. Cada fotograma de la animación se compone de una o varias imágenes de mapa de bits. Las imágenes pueden ser tan pequeñas como se necesiten o tan grandes como el propio marco.

Los detalles de animación, como el parpadeo ocular o el movimiento de los dedos, se pueden incluir como imágenes adicionales para el marco. Puede superponer varias imágenes para crear un compuesto y variar su posición en las capas. Esta técnica permite reutilizar imágenes en varios marcos y variar los detalles que cambian. Por ejemplo, si desea tener una onda de caracteres a mano, para cada fotograma podría usar una imagen base con todo, pero con la mano y superponer la imagen base con una imagen diferente. Del mismo modo, si desea que el carácter parpadee, puede superponer un conjunto diferente de ojos sobre una imagen base para cada fotograma. Las imágenes también se pueden desplazar a partir de la imagen base. Sin embargo, solo se mostrará la parte de la imagen que existe en el tamaño del marco.

Puede tener tantos fotogramas como desee en una animación. sin embargo, una animación típica calcula el promedio de 14 fotogramas para que se reproduzca durante más de seis segundos. Esta modesta cantidad de tiempo garantiza que el personaje parezca responder a los datos proporcionados por el usuario. Además, cuanto mayor sea el número de fotogramas, mayor será el archivo de animación. En el caso de los caracteres basados en Web descargados, mantenga el tamaño del archivo de animación lo más pequeño posible sin dejar de proporcionar un conjunto de fotogramas de tamaño razonable, de modo que la animación del carácter no parezca entrecortado.

### <a name="image-design"></a>Diseño de imagen

Puede usar cualquier herramienta de gráficos o animación para crear imágenes para fotogramas de animación, siempre que almacene las imágenes finales en el mapa de bits de Windows (. BMP). Cuando se crean las imágenes, use el editor de caracteres del agente de Microsoft (disponible en el [descargable](https://www.microsoft.com/download/en/details.aspx?id=14765)) para ensamblar, secuenciar y tiempo las imágenes, proporcionar otra información de caracteres y compilar toda la información en un archivo de caracteres final.

Las imágenes de caracteres deben estar diseñadas para una paleta de 256 colores, conservando los 20 colores del sistema de Windows estándar en su posición estándar en la paleta (las primeras 10 y las últimas 10 posiciones). Esto significa que la paleta de colores del carácter puede usar los colores estándar del sistema y hasta 236 otros colores. Al definir la paleta, incluya todas las propiedades que use el carácter en la animación. Si la paleta de caracteres coloca colores en las posiciones de color del sistema, esos colores de caracteres se sobrescribirán con los colores del sistema cuando el agente de Microsoft cree la paleta.

Cuanto mayor sea el número de colores que se usan en la paleta de colores de un carácter, mayor será la posibilidad de que la parte de los colores del carácter se reasigne para sistemas configurados con una configuración de color de 8 bits (256). Considere también el uso de la paleta de la aplicación en la que se utilizará el carácter. Es mejor evitar que el carácter reasigne los colores de su aplicación host y viceversa. Del mismo modo, si tiene previsto admitir varios caracteres que se muestran al mismo tiempo, probablemente querrá mantener una paleta coherente para esos caracteres. Puede considerar la posibilidad de usar solo los colores del sistema estándar en el carácter si tiene como destino una configuración de color de 8 bits. Sin embargo, es posible que esto no impida la reasignación del color del carácter si otra aplicación vuelve a definir la paleta de colores. En los sistemas establecidos en resoluciones de color más altas, la reasignación de paletas de colores no debe ser un problema, ya que el sistema administra automáticamente las paletas de colores.

El uso de un número mayor de colores en una imagen también puede aumentar el tamaño total del archivo de animación. El número de colores y la frecuencia de la variación puede determinar cómo se comprime el archivo de caracteres. Por ejemplo, un carácter bidimensional que usa solo unos pocos colores se comprimirá mejor que un carácter sombreado tridimensional.

Debe usar la misma paleta de colores para todo el archivo de caracteres. No se puede cambiar la paleta para distintas animaciones. Si intenta admitir configuraciones de color de 8 bits, considere la posibilidad de usar la misma paleta para la aplicación y cualquier otro carácter que tenga previsto admitir.

La posición<sup>11 en</sup> la paleta se define de forma predeterminada como el color de transparencia (o alfa), aunque también se puede establecer el color mediante el editor de caracteres del agente de Microsoft. Los servicios de animación de agente de Microsoft representan transparentes en este color, por lo que debe usar el color de las imágenes solo donde quiera transparencia.

Considere cuidadosamente la forma del carácter, ya que puede afectar al rendimiento de la animación. Para mostrar el carácter, los servicios de animación crean una ventana de región basada en la imagen global. Las pequeñas áreas irregulares suelen requerir más datos de la región y pueden reducir el rendimiento de la animación del carácter. Por lo tanto, cuando sea posible, evite huecos o elementos de un solo píxel y detalles.

Evite el suavizado de contorno del borde exterior del carácter. Aunque el suavizado de contorno es una buena técnica para reducir los bordes dentados, se basa en colores adyacentes. Dado que el carácter puede aparecer encima de una variedad de colores, el suavizado de contorno del borde exterior puede hacer que el carácter parezca deficiente con respecto a otros. Sin embargo, puede usar el suavizado de contorno en los detalles internos del carácter sin que se produzca este problema.

### <a name="frame-size"></a>Tamaño de marco

Normalmente, el tamaño del marco no debe ser superior a 128 x 128 píxeles. Aunque los caracteres pueden ser más grandes o más pequeños en cualquiera de las dimensiones, el editor de caracteres del agente de Microsoft los usa como tamaño de presentación y escala las imágenes de caracteres si se define un tamaño de fotograma mayor. El tamaño de fotograma 128 x 128 realiza un equilibrio razonable con el espacio que el carácter ocupará en la pantalla. La aplicación puede escalar un carácter en tiempo de ejecución.

### <a name="frame-duration"></a>Duración del marco

Puede usar el editor de caracteres del agente de Microsoft para establecer cuánto tiempo se mostrará cada fotograma de la animación antes de pasar al siguiente fotograma. Establezca la duración de cada fotograma en al menos 10 centésimas de segundo (10 fotogramas por segundo), todo lo que menos no sea perceptible en algunos sistemas. También puede establecer la duración más larga, pero evitar pausas no naturales en la acción.

El editor de caracteres del agente de Microsoft también admite la bifurcación de un fotograma de una animación a otra, en función de los porcentajes de probabilidad que suministre. Para cualquier fotograma determinado, puede definir hasta tres ramas diferentes. La bifurcación permite crear animaciones que varían cuando se reproducen y animaciones que se repiten. Sin embargo, tenga cuidado al usar la bifurcación, ya que puede crear problemas al intentar reproducir una animación después de otra. Por ejemplo, si reproduce una animación de bucle o de bifurcación, podría continuar indefinidamente a menos que use un método [**Stop**](stop-method.md) . Si no está seguro, evite la bifurcación.

Los fotogramas que no tienen imágenes y se establecen en cero Duration no aparecen cuando se incluyen en una animación. Puede usar esta característica para crear fotogramas que admitan la bifurcación sin ser visibles. Sin embargo, se mostrará un fotograma que no tenga imágenes todavía con una duración mayor que cero. Por lo tanto, evite incluir marcos vacíos en la animación, ya que es posible que el usuario no pueda distinguir un fotograma vacío de cuando el carácter esté oculto.

### <a name="frame-transition"></a>Transición de fotogramas

Al diseñar una animación, considere la posibilidad de realizar una transición fluida desde y hacia la animación. Por ejemplo, si crea una animación en la que los gestos de caracteres son correctos y otro en el que los gestos de caracteres están a la izquierda, quiere que el carácter se anime sin problemas de una posición a otra. Aunque podría compilarlo en cualquiera de las animaciones, una solución mejor es definir una posición neutra o transitoria desde la que se inicia y devuelve el carácter. La animación a la posición neutra se puede incorporar como parte de cada animación o como una animación independiente. En el editor de caracteres del agente de Microsoft, puede especificar una animación de **devolución** complementaria para cada animación del carácter. Normalmente, la animación **devuelta** no debe tener más de 2-4 fotogramas, por lo que el carácter puede pasar rápidamente a la posición neutra.

Por ejemplo, con el escenario "gesturing Right, después gesturing left", puede crear una animación **GestureRight** , comenzando por un fotograma donde el carácter aparece en una posición neutra y agregar fotogramas con imágenes que extienden la mano del carácter hacia la derecha. A continuación, cree la animación de **retorno** : una animación complementaria con imágenes que devuelven el carácter a su posición neutra. Puede asignarlo como la animación de devolución para la animación **GestureRight** . A continuación, cree la animación **GestureLeft** que comienza en la posición neutra y extiende el brazo del carácter hacia la izquierda. Por último, también se crea una animación de **devolución** complementaria para esta animación. Normalmente, una animación de **devolución** comienza con una imagen que sigue a la última imagen de la animación anterior.

Iniciar y volver a la misma posición neutra, ya sea dentro de una animación o mediante una animación de devolución, le permite reproducir cualquier animación en cualquier orden. Los servicios de animación de agente de Microsoft reproducen automáticamente la animación de devolución designada en muchas situaciones. Por ejemplo, los servicios juegan la animación de **devolución** designada antes de reproducir las animaciones de estado de ralentí del carácter. Es una buena idea definir y asignar animaciones **devueltas** si las animaciones no terminan en la posición neutra.

Si desea proporcionar sus propias transiciones entre animaciones específicas; por ejemplo, dado que siempre se reproduce en un orden bien definido, puede evitar definir animaciones de **devolución** . Sin embargo, sigue siendo una buena idea comenzar y finalizar la secuencia de animaciones de la posición neutra.

### <a name="speaking-animation"></a>Animación en voz

Proporcione imágenes de la boca para cada animación en la que desee que el carácter pueda hablar, a menos que el diseño del carácter no tenga ninguna boca o indicación animada de la salida de voz. En general, el movimiento de la boca es muy importante. Un carácter puede parecer menos inteligente, likable o honesto si el movimiento de la boca no se sincroniza de forma razonable con su voz. Las imágenes de la boca permiten que el personaje se sincronice con la salida de voz. Las imágenes de la boca se definen por separado y como archivos de mapa de bits de Windows. Deben coincidir con la misma paleta de colores que las demás imágenes de la animación.

Los servicios de animación de agente de Microsoft muestran fotogramas de animación en la parte superior del último fotograma de una animación, también denominado el *marco de habla* de la animación. Por ejemplo, cuando el carácter habla en la animación **GestureRight** , los servicios de animación superponen los fotogramas de animación en el último fotograma de **GestureRight**. Un carácter no puede hablar mientras se anima, por lo que solo suministra imágenes de la boca para el último fotograma de una animación. Además, el marco de habla debe ser el marco final de una animación, por lo que un carácter no puede hablar en una animación de bucle.

Normalmente, se proporcionan las imágenes de la boca en el mismo tamaño que el marco (y la imagen base), pero solo se incluye el área que anima como parte del movimiento de la boca y se representa el resto de la imagen en el color transparente. Diseñe la imagen para que coincida con la imagen del marco de habla cuando se superpone encima de ella. Para que coincida correctamente, es probable que necesite crear un conjunto independiente de imágenes de la boca para cada animación en la que habla el carácter.

Una imagen de la boca puede incluir más que la boca, como el mecanizado u otras partes del cuerpo del carácter mientras habla. Sin embargo, si mueve una mano o una pierna, tenga en cuenta que puede parecer que se mueve aleatoriamente porque la superposición de la boca mostrada se basará en el fonema actual de una frase hablada. Además, el servidor recorta la imagen de la boca en el contorno de la imagen del marco de habla. Diseñe la imagen de superposición de la boca para que permanezca dentro del contorno de su imagen de marco de habla de base, porque el servidor usa la imagen base para crear el límite de la ventana para el carácter.

El editor de caracteres del agente de Microsoft permite definir siete posiciones básicas que se corresponden con las formas de boca de fonema comunes que se muestran en la tabla siguiente:

**Imágenes de animación de la boca**



| Posición de la boca | Imagen de ejemplo                       | Representación                                                                                                                     |
|----------------|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| Closed         | :::image type="icon" source="images/g07ci01.gif":::<br/> | Forma cerrada normal. También se usa para fonemas como "m" como en "Mom", "b" como en "Bob", "f", como en "Fife".<br/>           |
| En todo el mundo abierto 1    | :::image type="icon" source="images/g07ci02.gif":::<br/> | La boca está ligeramente abierta, con un ancho completo. Se usa para fonemas como "g" como en "gag", "l" como en "periodo", "EAR" como en "escuchar".<br/> |
| En todo el mundo abierto 2    | :::image type="icon" source="images/g07ci03.gif":::<br/> | La boca está parcialmente abierta, con un ancho completo. Se usa para fonemas como "n" como en "Nun", "d" como en "dad", "t", como en "Tot".<br/>    |
| En todo el mundo abierto 3    | :::image type="icon" source="images/g07ci04.gif":::<br/> | La boca está abierta, con un ancho completo. Se usa para fonemas como "u" como en "apagar", "EA" como en "Head", "Your" como en "lesiona".<br/>          |
| Todo abierto 4    | :::image type="icon" source="images/g07ci05.gif":::<br/> | La boca está completamente abierta, con un ancho completo. Se usa para fonemas como "a" como en "Hat", "ostrar" como "cómo..."<br/>                   |
| Abierto-medio    | :::image type="icon" source="images/g07ci06.gif":::<br/> | La boca está abierta a mitad de ancho. Se usa para fonemas como "Oy" como en "Ahoy", "o" como en "calor".<br/>                              |
| Abrir-estrecho    | :::image type="icon" source="images/g07ci07.gif":::<br/> | La boca está abierta en ancho estrecho. Se usa para fonemas como "o" como en "circular", "o" como "Espero", "w", como en "húmedo".<br/>           |



 

 

 





