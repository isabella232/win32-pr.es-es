---
description: Un dispositivo de teléfono es un dispositivo que admite la clase de dispositivo de teléfono y que incluye interruptores de enlace, teléfonos móviles, teléfonos de altavoz y cascos.
ms.assetid: c2660d77-0265-49d4-bd04-1cddd674b760
title: Teléfono Elementos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5744967dc738a65d7632dc1a1f6126bfbc9887
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071096"
---
# <a name="phone-device-elements"></a>Teléfono Elementos de dispositivo

Un dispositivo de teléfono es un dispositivo que admite la clase de dispositivo de teléfono y que incluye algunos o todos los elementos siguientes:

-   **Hookswitch/hookswitch:** se trata de un medio para la entrada y salida de audio. Un dispositivo de teléfono puede tener varios artefactos, que se pueden activar y desactivar (quitar o colocar enhook) bajo el control manual o de aplicación del usuario.

    La telefonía identifica tres tipos de dispositivos de conmutador de enlace comunes a muchos conjuntos de teléfonos:

     **Handset**: la combinación tradicional de piezas de manos y oídos que se deben elevar manualmente de una almohadilla y mantenerla en la oído del usuario.  
    **Speakerphone:** permite al usuario realizar llamadas sin manos. El altavoz puede ser interno o externo al dispositivo del teléfono. La parte del hablante de un speakerphone permite varios agentes de escucha.  
    **Casco:** permite al usuario realizar llamadas sin manos.  
    

    Un conmutador de enlace debe ser un offhook para permitir que los datos de audio se envíen o reciban por parte del correspondiente objeto.

-   Control de volumen/Control de ganancia/Exclusión mutua: cada dispositivo de conmutador de enlace es el emparejamiento de un altavoz y un componente de micrófono. La API proporciona control de volumen y muting de componentes de altavoz y para obtener control o muting de componentes de micrófono.
-   [Timbre:](ring.md)un medio para alertar a los usuarios, normalmente a través de una campana. Un dispositivo de teléfono puede ser capaz de sonar en una variedad de modos o patrones.
-   [Mostrar:](display.md)un mecanismo para presentar visualmente mensajes al usuario. Una pantalla de teléfono se caracteriza por su número de filas y columnas.
-   [Teléfono botones:](phone-buttons.md)una matriz de botones. Cada vez que el usuario presiona un botón en el conjunto de teléfonos, la API informa de que se ha presionado el botón correspondiente. Los identificadores de la bombilla de botón identifican un par de botones y bombillas. Por supuesto, es posible tener pares de botón-bombilla sin botón o sin ninguna bombilla. Los identificadores de bombilla de botón son valores enteros que oscilan entre 0 y el número máximo de bombillas de botón disponibles en el dispositivo del teléfono, menos uno. Cada botón pertenece a una clase de botón. Las clases incluyen botones de apariencia de llamadas, botones de características, botones del teclado y botones locales.
-   [Lamps](lamps.md): una matriz de bombillas (por ejemplo, LED) que se pueden controlar individualmente desde la API. Las bombillas se pueden encender en diferentes modos variando la frecuencia de encendido y apagado. El identificador de la bombilla de botón identifica la bombilla.
-   [Áreas de](data-areas.md)datos: áreas de memoria en el dispositivo telefónico desde las que se puede descargar o cargar el código de instrucción o los datos. La información descargada afectaría al comportamiento (o, en otras palabras, al programa) del dispositivo telefónico.

TAPI permite que una aplicación supervise y controle los elementos del dispositivo telefónico. Los elementos más útiles para una aplicación son los dispositivos hookswitch. El conjunto de teléfonos puede actuar como un dispositivo de E/S de audio (en el equipo) con control de volumen, obtener control y silenciar, un timbre (para alertar al usuario), áreas de datos (para programar el teléfono) y quizás una pantalla, aunque la pantalla del equipo sea más capaz. No se recomienda que el escritor de aplicaciones controle directamente o use bombillas de teléfono o botones de teléfono, ya que las funcionalidades de las bombillas y los botones pueden variar ampliamente entre los conjuntos de teléfonos, y las aplicaciones pueden adaptarse rápidamente a determinados conjuntos de teléfonos.

No hay ningún conjunto básico garantizado de servicios admitidos por todos los dispositivos de teléfono, ya que existe para los dispositivos de línea (los servicios de telefonía básica). Por lo tanto, antes de que una aplicación pueda usar un dispositivo de teléfono, la aplicación debe determinar primero las funcionalidades exactas del dispositivo telefónico. La funcionalidad de telefonía varía según la configuración (cliente frente a cliente/servidor), el hardware telefónico y el software del proveedor de servicios. Las aplicaciones no deben realizar suposiciones sobre qué funcionalidades de telefonía están disponibles. Una aplicación determina las funcionalidades de un dispositivo telefónico mediante una llamada a la [**función phoneGetDevCaps.**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) Las funcionalidades del dispositivo de un teléfono indican cuáles de estos elementos existen para cada dispositivo de teléfono presente en el sistema y cuáles son sus funcionalidades. Aunque está fuertemente orientada a los conjuntos de teléfonos de la vida real, esta abstracción también puede proporcionar una implementación significativa (o subconjunto de los mismos) para otros dispositivos. Tome como ejemplo un casco independiente conectado directamente y controlable desde el equipo y que funciona como un dispositivo de teléfono. Los cambios del conmutador de enlace se pueden desencadenar mediante la detección de energía de voz (offhook) o un período de silencio (onhook). el timbre se puede emular mediante la generación de una señal de sonido en el casco. una pantalla se puede emular mediante la conversión de texto a voz.

No es necesario realizar un dispositivo de teléfono en hardware, sino que se puede emular en software mediante una interfaz gráfica de comandos controlada por mouse o teclado y el altavoz o el sistema de sonido del equipo. Este tipo de "teléfono flexible" puede ser una aplicación que usa TAPI. También puede ser un proveedor de servicios, que puede aparecer como un dispositivo de teléfono disponible para otras aplicaciones a través de la API y, como tal, se le asigna un identificador de dispositivo de teléfono.

Según el entorno y la configuración, los conjuntos de teléfonos pueden ser dispositivos compartidos entre la aplicación y el conmutador. Se realiza algún aprovisionamiento menor en la API, donde el conmutador puede suspender temporalmente el control de la API de un dispositivo telefónico.

 

 



