---
title: Animaciones
description: Animaciones
ms.assetid: 8bd9ac94-3f86-4168-bf33-7a2c8d11907d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ac361815575feab5bfbfbadbf4feaf7258fbbef31f8634b6b34d222d46d274
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117694209"
---
# <a name="animations"></a>Animaciones

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Las animaciones de un carácter reflejan su sexo, edad, personalidad y comportamiento. El número y los tipos de animaciones que cree para un carácter dependen de lo que haga el carácter y de cómo responda a diferentes situaciones.

Al igual que las animaciones tradicionales, las animaciones digitales implican la creación de una serie de imágenes ligeramente diferentes que, cuando se muestran secuencialmente, proporcionan la dicha de acción. La creación de imágenes de animación de alta calidad puede requerir un animador cualificado, pero el estilo y la presentación del carácter que cree también afectan a la calidad. Los caracteres bidimensionales con formas y características simples a veces pueden ser tan eficaces como (o más eficaces que) caracteres altamente representados. No es necesario crear una imagen realista para representar un carácter efectivo. Muchos caracteres populares de dibujos animados no son realistas en su presentación, pero son eficaces porque el animador entiende cómo transmitir la acción y la emoción. El apéndice proporciona información general sobre los principios fundamentales de diseño de animación.

### <a name="frames"></a>Marcos

Cada animación que se crea para un carácter de Microsoft Agent se compone de una secuencia de fotogramas con tiempo. Cada fotograma de la animación se compone de una o varias imágenes de mapa de bits. Las imágenes pueden ser tan pequeñas como se necesiten o tan grandes como el propio marco.

Los detalles de animación, como el parpadeo de los ojos o el movimiento de los dedos, se pueden incluir como imágenes adicionales para el marco. Puede superponer varias imágenes para crear un compuesto y variar su posición en las capas. Esta técnica permite reutilizar imágenes en varios fotogramas y variar los detalles que cambian. Por ejemplo, si desea que un carácter ondee su mano, para cada fotograma podría usar una imagen base con todo menos la mano y superponer la imagen base con una imagen de mano diferente. Del mismo modo, si desea que el carácter parpadee, puede superponer un conjunto diferente de ojos sobre una imagen base para cada fotograma. Las imágenes también se pueden desplazar de la imagen base. Sin embargo, solo se mostrará la parte de la imagen que existe dentro del tamaño del marco.

Puede tener tantos fotogramas en una animación como desee; sin embargo, una animación típica promedia unos 14 fotogramas para que no se resalte durante más de seis segundos. Esta cantidad de tiempo moderada garantiza que el carácter parece responder a la entrada del usuario. Además, cuanto mayor sea el número de fotogramas, mayor será el archivo de animación. En el caso de los caracteres basados en web descargados, mantenga el tamaño del archivo de animación lo más pequeño posible y, al mismo tiempo, proporcione un conjunto de fotogramas con un tamaño razonable, de modo que la animación del carácter no parezca desasistido.

### <a name="image-design"></a>Diseño de imágenes

Puede usar cualquier herramienta de gráficos o animación para crear imágenes para fotogramas de animación, siempre que almacene las imágenes finales en el formato Windows mapa de bits (.BMP). Cuando se crean las imágenes, use el Editor de caracteres del agente de Microsoft (disponible en el archivo [descargable)](https://www.microsoft.com/download/en/details.aspx?id=14765)para ensamblar, secuenciar y time las imágenes, proporcionar otra información de caracteres y compilar toda la información en un archivo de caracteres final.

Las imágenes de caracteres deben diseñarse en una paleta de 256 colores, conservando los 20 colores estándar del sistema Windows en su posición estándar en la paleta (las 10 primeras y las últimas 10 posiciones). Esto significa que la paleta de colores del carácter puede usar los colores estándar del sistema y hasta 236 colores más. Al definir la paleta, incluya cualquier propiedad que el carácter use en la animación. Si la paleta de caracteres coloca los colores en las posiciones de color del sistema, esos colores de caracteres se sobrescribirán con los colores del sistema cuando Microsoft Agent cree la paleta.

Cuanto mayor sea el número de colores que use en la paleta de colores de un carácter, mayor será la posibilidad de que parte de los colores del carácter se pueda volver a ajustar para los sistemas configurados en una configuración de color de 8 bits (256). Considere también el uso de la paleta de la aplicación en la que se usará el carácter. Es mejor evitar que el carácter vuelva a asignar los colores de su aplicación host y viceversa. Del mismo modo, si tiene previsto admitir varios caracteres que se muestran al mismo tiempo, probablemente querrá mantener una paleta coherente para esos caracteres. Puede considerar la posibilidad de usar solo los colores estándar del sistema en el carácter si tiene como destino usuarios con una configuración de color de 8 bits. Sin embargo, es posible que esto no impida la remapping del color del carácter si otra aplicación redefine ampliamente la paleta de colores. En los sistemas establecidos en resoluciones de colores más altas, la remapping de la paleta de colores no debe ser un problema porque el sistema administra las paletas de colores automáticamente.

El uso de un mayor número de colores en una imagen también puede aumentar el tamaño total del archivo de animación. El número de colores y la frecuencia de variación pueden determinar el nivel de compresión del archivo de caracteres. Por ejemplo, un carácter bidimensional que usa solo unos pocos colores se comprimirá mejor que un carácter tridimensional sombreado.

Debe usar la misma paleta de colores para todo el archivo de caracteres. No se puede cambiar la paleta para diferentes animaciones. Si intenta admitir configuraciones de color de 8 bits, considere la posibilidad de usar la misma paleta para la aplicación y cualquier otro carácter que planee admitir.

La posición<sup>11</sup> de la paleta se define de forma predeterminada como color de transparencia (o alfa), aunque también puede establecer el color mediante el Editor de caracteres de Microsoft Agent. Los servicios de animación de Microsoft Agent representan transparentes los píxeles de este color, así que use el color de las imágenes solo donde quiera transparencia.

Considere cuidadosamente la forma del carácter, ya que puede afectar al rendimiento de la animación. Para mostrar el carácter, los servicios de animación crean una ventana de región basada en la imagen general. Las áreas irregulares pequeñas a menudo requieren más datos de región y pueden reducir el rendimiento de animación del carácter. Por lo tanto, cuando sea posible, evite espacios o elementos y detalles de un solo píxel.

Evite suavizar el alias del borde exterior del carácter. Aunque el suavizado de contorno es una buena técnica para reducir los bordes irregulares, se basa en colores adyacentes. Dado que el carácter puede aparecer encima de una variedad de colores, el suavizado de alias del borde exterior puede hacer que el carácter aparezca mal en otros fondos. Sin embargo, puede usar suavizado de alias en los detalles interiores del carácter sin encontrar este problema.

### <a name="frame-size"></a>Tamaño del marco

Normalmente, el tamaño del marco no debe ser superior a 128 x 128 píxeles. Aunque los caracteres pueden ser mayores o más pequeños en cualquiera de las dos dimensiones, el Editor de caracteres de Microsoft Agent lo usa como tamaño de presentación y escala las imágenes de caracteres si define un tamaño de fotograma mayor. El tamaño de fotograma de 128 x 128 hace que el espacio que ocupará el carácter en la pantalla sea razonable. La aplicación puede escalar un carácter en tiempo de ejecución.

### <a name="frame-duration"></a>Duración del fotograma

Puede usar el Editor de caracteres de Microsoft Agent para establecer cuánto tiempo se mostrará cada fotograma de animación antes de pasar al fotograma siguiente. Establezca la duración de cada fotograma en al menos 10 centésimas de segundo (10 fotogramas por segundo), algo menos que podría no ser perceptible en algunos sistemas. También puede establecer la duración más larga, pero evitar pausas no naturales en la acción.

El Editor de caracteres de Microsoft Agent también admite la bifurcación de un fotograma de una animación a otro, en función de los porcentajes de probabilidad que proporcione. Para cualquier fotograma determinado, puede definir hasta tres bifurcaciones diferentes. La bifurcación permite crear animaciones que varían cuando se reproducen y animaciones que se recorren en bucle. Sin embargo, tenga cuidado al usar la bifurcación, ya que puede crear problemas al intentar reproducir una animación después de otra. Por ejemplo, si reproduce una animación de bucle o bifurcación, podría continuar indefinidamente a menos que use un [**método Stop.**](stop-method.md) Si no está seguro, evite la bifurcación.

Los fotogramas que no tienen imágenes y están establecidos en duración cero no aparecen cuando se incluyen en una animación. Puede usar esta característica para crear fotogramas que admitan la bifurcación sin ser visibles. Sin embargo, se mostrará un marco que aún no tiene imágenes con una duración mayor que cero. Por lo tanto, evite incluir fotogramas vacíos en la animación, ya que es posible que el usuario no pueda distinguir un fotograma vacío de cuando el carácter está oculto.

### <a name="frame-transition"></a>Transición de fotogramas

Al diseñar una animación, tenga en cuenta cómo realizar la transición sin problemas desde y hacia la animación. Por ejemplo, si crea una animación en la que el carácter se mueve a la derecha y otra en la que el carácter se mueve a la izquierda, quiere que el carácter se animara sin problemas de una posición a la otra. Aunque podría crear esto en cualquiera de las animaciones, una mejor solución es definir una posición neutra o transitoria desde la que se inicia y devuelve el carácter. La animación a la posición neutra se puede incorporar como parte de cada animación o como una animación independiente. En el Editor de caracteres de Microsoft Agent, puede especificar una animación **Return** complementaria para cada animación del carácter. La **animación Devolución** normalmente no debe tener más de 2-4 fotogramas, por lo que el carácter puede pasar rápidamente a la posición neutra.

Por ejemplo, con el escenario "gesturing right, then gesturing left" (gesturing right, then gesturing left), puede crear una animación **GestureRight,** empezando por un marco en el que el carácter aparece en una posición neutra, y agregar fotogramas con imágenes que extienden la mano del carácter a la derecha. A continuación, **cree su animación Return:** animación complementaria con imágenes que devuelven el carácter a su posición neutra. Puede asignarlo como animación Devolución para la **animación GestureRight.** A continuación, cree la **animación GestureLeft** que comienza desde la posición neutra y extiende el arm del carácter a la izquierda. Por último, cree también una **animación Return** complementaria para esta animación. **Normalmente,** una animación Return comienza con una imagen que sigue a la última imagen de la animación anterior.

Iniciar y volver a la misma posición neutra, ya sea dentro de una animación o mediante una animación Devolución, permite reproducir cualquier animación en cualquier orden. Los servicios de animación de Microsoft Agent reproducen automáticamente la animación Return designada en muchas situaciones. Por ejemplo, los servicios reproducen la animación **Return** designada antes de reproducir las animaciones de estado idling del carácter. Es una buena idea definir y asignar animaciones **Return** si las animaciones aún no terminan en la posición neutra.

Si desea proporcionar sus propias transiciones entre animaciones específicas; Por ejemplo, dado que siempre se reproducen en un orden bien definido, puede evitar definir **animaciones Return.** Sin embargo, sigue siendo una buena idea comenzar y finalizar la secuencia de animaciones desde la posición neutra.

### <a name="speaking-animation"></a>Animación de habla

Proporcione imágenes de fondo para cada animación durante la que quiera que el carácter pueda hablar, a menos que el diseño del carácter no tenga ninguna voz animada ni indicación de salida hablada. En general, el movimiento de la marcha es muy importante. Un carácter puede parecer menos inteligente, menos inteligente o más inteligente si su movimiento de la charla no está razonablemente sincronizado con su voz. Las imágenes de sonido permiten que el carácter se sincronice con la salida hablada. Las imágenes de fondo se definen por separado y como Windows de mapa de bits. Deben coincidir con la misma paleta de colores que las demás imágenes de la animación.

Los servicios de animación de Microsoft Agent muestran fotogramas de animación en la parte superior del último fotograma de una animación, también denominado marco de *habla* de la animación. Por ejemplo, cuando el carácter habla en la animación **GestureRight,** los servicios de animación superponen los fotogramas de animación de la máscara en el último fotograma de **GestureRight.** Un carácter no puede hablar mientras se anima, por lo que solo se suministran imágenes de cocina para el último fotograma de una animación. Además, el marco de habla debe ser el fotograma final de una animación, por lo que un carácter no puede hablar en una animación en bucle.

Normalmente, proporcionaría las imágenes de la cocina en el mismo tamaño que el marco (y la imagen base), pero incluiría solo el área que se anima como parte del movimiento de la cocina y representaría el resto de la imagen en el color transparente. Diseñe la imagen para que coincida con la imagen en el marco de habla cuando se superlate encima de ella. Para que coincida correctamente, es probable que tenga que crear un conjunto independiente de imágenes de cocina para cada animación en la que habla el carácter.

Una imagen de cocina puede incluir más que la propia cocina, como la chin u otras partes del cuerpo del carácter mientras habla. Sin embargo, si mueve una mano o una mano, tenga en cuenta que puede parecer que se mueve aleatoriamente porque la superposición de la máscara mostrada se basará en el phoneme actual de una frase hablada. Además, el servidor recorta la imagen de la charla al contorno de la imagen del marco de habla. Diseñe la imagen de superposición de la máscara para que permanezca dentro del contorno de su imagen de marco de habla base, ya que el servidor usa la imagen base para crear el límite de la ventana para el carácter.

El Editor de caracteres de Microsoft Agent le permite definir siete posiciones básicas de la manita que corresponden a formas comunes de forma de ómeme que se muestran en la tabla siguiente:

**Imágenes de animación de animación de fondo**



| Posición de la posición de la posición de | Imagen de ejemplo                       | Representación                                                                                                                     |
|----------------|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| Closed         | :::image type="icon" source="images/g07ci01.gif":::<br/> | Forma cerrada normal. También se usa para phonemes como "m" como en "mom", "b" como en "bob", "f" como en "fife".<br/>           |
| Open-wide 1    | :::image type="icon" source="images/g07ci02.gif":::<br/> | La cocina está ligeramente abierta, con ancho completo. Se usa para phonemes como "g" como en "gh", "l" como en "lull", "ear" como en "hear".<br/> |
| Open-wide 2    | :::image type="icon" source="images/g07ci03.gif":::<br/> | La cocina está parcialmente abierta, con ancho completo. Se usa para phonemes como "n" como en "geno", "d" como en "padre", "t" como en "tot".<br/>    |
| Open-wide 3    | :::image type="icon" source="images/g07ci04.gif":::<br/> | La cocina está abierta, con ancho completo. Se usa para phonemes como "u" como en "pizza", "ea" como en "head", "your" como en "daño".<br/>          |
| Open-wide 4    | :::image type="icon" source="images/g07ci05.gif":::<br/> | La cocina está completamente abierta, con ancho completo. Se usa para phonemes como "a" como en "hat", "ow" como en "how".<br/>                   |
| Medio abierto    | :::image type="icon" source="images/g07ci06.gif":::<br/> | La cocina está abierta a medio ancho. Se usa para phonemes como "oy" como en "ahoy", "o" como en "hot".<br/>                              |
| Open-narrow    | :::image type="icon" source="images/g07ci07.gif":::<br/> | La cocina está abierta a un ancho estrecho. Se usa para phonemes como "o" como en "insond", "o" como en "hope", "w" como en "wet".<br/>           |



 

 

 





