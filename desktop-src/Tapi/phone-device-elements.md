---
description: Un dispositivo telefónico es un dispositivo que admite la clase de dispositivo de teléfono y que incluye hookswitches, auriculares, altavoz y auriculares.
ms.assetid: c2660d77-0265-49d4-bd04-1cddd674b760
title: Elementos de dispositivo de teléfono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5744967dc738a65d7632dc1a1f6126bfbc9887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677936"
---
# <a name="phone-device-elements"></a>Elementos de dispositivo de teléfono

Un dispositivo telefónico es un dispositivo que admite la clase de dispositivo de teléfono y que incluye algunos o todos los elementos siguientes:

-   **Conmutador/transductor**: es un medio para la entrada y salida de audio. Un dispositivo telefónico puede tener varios transductores, que se pueden activar y desactivar (tomar OffHook o enlazó) en el control de usuario de la aplicación o manual.

    La telefonía identifica tres tipos de dispositivos conmutador comunes a muchos conjuntos de teléfonos:

     **Auricular**: la combinación tradicional de la boca y la lengüeta que debe levantarse manualmente de una base y mantenerse en la lengüeta del usuario.  
    **Altavoz**: permite al usuario realizar llamadas sin complicaciones. El altavoz puede ser interno o externo al dispositivo telefónico. La parte del hablante de un altavoz permite varios agentes de escucha.  
    **Auriculares**: permite al usuario realizar llamadas sin complicaciones.  
    

    Un conmutador debe ser OffHook para permitir que el transductor correspondiente envíe o reciba datos de audio.

-   Control de volumen/control de ganancia/silencio: cada dispositivo conmutador es el emparejamiento de un altavoz y un componente de micrófono. La API proporciona control de volumen y silenciamiento de los componentes de altavoz y para obtener control o silenciar los componentes de micrófono.
-   [Timbre](ring.md): un medio para avisar a los usuarios, normalmente a través de una campana. Un dispositivo telefónico puede sonar en varios modos o patrones.
-   [Display](display.md): un mecanismo para presentar visualmente los mensajes al usuario. Una presentación de teléfono se caracteriza por su número de filas y columnas.
-   [Botones de teléfono](phone-buttons.md): una matriz de botones. Siempre que el usuario presiona un botón en el juego de teléfono, la API informa de que se presionó el botón correspondiente. Los identificadores de luz de botón identifican un par de botón y lámpara. Por supuesto, es posible tener pares de luz de botón con un botón o sin luz. Los identificadores de luz de botón son valores enteros comprendidos entre 0 y el número máximo de lámparas de botón disponibles en el dispositivo telefónico, menos uno. Cada botón pertenece a una clase de botón. Las clases incluyen botones de apariencia de llamadas, botones de características, botones de teclado y botones locales.
-   [Lámparas](lamps.md): una matriz de lámparas (como LED) que se controla de forma individual desde la API. Las lámparas se pueden iluminar en modos diferentes mediante la variación de la frecuencia de encendido y apagado. El identificador de la lámpara de botón identifica la lámpara.
-   [Áreas de datos](data-areas.md): áreas de memoria del dispositivo telefónico donde el código o los datos de la instrucción se pueden descargar o cargar desde. La información descargada afectaría al comportamiento (o en otras palabras, programa) del dispositivo de teléfono.

TAPI permite que una aplicación supervise y controle los elementos del dispositivo telefónico. Los elementos más útiles para una aplicación son los dispositivos conmutador. El juego de teléfono puede actuar como un dispositivo de e/s de audio (para el equipo) con control de volumen, obtener control y silenciar un timbre (para avisar al usuario), áreas de datos (para programar el teléfono) y quizás una pantalla, aunque la pantalla del equipo sea más capaz. No se recomienda que el escritor de la aplicación controle directamente o use las lámparas telefónicas o los botones de teléfono, ya que las capacidades de las lámparas y los botones pueden variar considerablemente entre los juegos de teléfono y las aplicaciones se pueden personalizar rápidamente a determinados conjuntos de teléfonos.

No hay ningún conjunto de servicios de nivel de servicio garantizado que admitan todos los dispositivos telefónicos, ya que se trata de dispositivos de línea (los servicios de telefonía básicos). Por lo tanto, antes de que una aplicación pueda usar un dispositivo de teléfono, la aplicación debe determinar primero las capacidades exactas del dispositivo de teléfono. La capacidad de telefonía varía en función de la configuración (cliente frente al cliente/servidor), el hardware telefónico y el software de proveedor de servicios. Las aplicaciones no deben suponer ninguna suposición sobre las capacidades de telefonía que están disponibles. Una aplicación determina las capacidades del dispositivo de un dispositivo telefónico mediante una llamada a la función [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) . Las capacidades de dispositivo de un teléfono indican cuál de estos elementos existen para cada dispositivo telefónico presente en el sistema y cuáles son sus capacidades. Aunque está fuertemente orientada hacia los conjuntos de teléfonos reales, esta abstracción puede proporcionar una implementación significativa (o subconjunto de la misma) también para otros dispositivos. Tome como ejemplo un casco independiente conectado y controlable directamente desde el equipo y administrado como dispositivo telefónico. Los cambios de conmutador se pueden desencadenar mediante la detección de energía de voz (OffHook) o un período de silencio (anzuelo). los anillos se pueden emular mediante la generación de una señal audible en el casco; una presentación se puede emular mediante conversión de texto a voz.

No es necesario que un dispositivo telefónico esté presente en el hardware, sino que se puede emular en el software mediante una interfaz gráfica de comandos basada en teclado o en el sistema y el altavoz del equipo. Este tipo de "teléfono flexible" puede ser una aplicación que utiliza TAPI. También puede ser un proveedor de servicios, que puede aparecer como un dispositivo telefónico disponible para otras aplicaciones a través de la API y, como tal, se le asigna un identificador de dispositivo de teléfono.

En función del entorno y de la configuración, los conjuntos de teléfonos pueden ser dispositivos compartidos entre la aplicación y el conmutador. En la API se realiza algún aprovisionamiento secundario, en el que el conmutador puede suspender temporalmente el control de la API de un dispositivo telefónico.

 

 



