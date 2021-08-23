---
title: Animar un carácter
description: Animar un carácter
ms.assetid: ed42de30-acac-41e8-bacb-4caaff254724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 937b970f1cdc9de9c973d298bbe963bfa70e4de3733869292e54d5d32742c722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976785"
---
# <a name="animating-a-character"></a>Animar un carácter

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Una vez cargado un carácter, puede usar varios de los métodos de Microsoft Agent para animar el carácter. El primero que se usa suele ser el [**método Show.**](show-method.md) **Mostrar** hace que el marco del carácter sea visible y reproduce la animación asignada al estado **Mostrando del** carácter.

Una vez que el marco del carácter está visible, puede usar el método [**Play,**](play-method.md) especificando el nombre de una animación, para reproducir esa animación. Los nombres de animación son específicos de una definición de caracteres. A medida que se reproduce una animación, la forma de su ventana cambia para que coincida con la imagen del marco. Esto da como resultado una imagen gráfica móvil, o *sprite,* que se muestra en la parte superior del escritorio y en todas las ventanas, o *bien en orden z.*

Si el archivo del carácter se almacena localmente, simplemente puede llamar al [**método Play.**](play-method.md) En otros casos, como cuando se ha cargado un . Carácter ACF de un servidor HTTP, debe usar el [**método Get**](get-method.md) (o [**Prepare)**](/windows/desktop/lwef/iagentcharacter--prepare)para recuperar primero los datos de animación. Esto hará que el Agente solicite el archivo de animación del servidor y lo almacene en el búfer del explorador en el equipo local.

El [**método Speak**](speak-method.md) permite programar el carácter para que hable, sincronizando automáticamente la salida. En la sección Salida de este documento se tratan más detalles.

Puede usar el [**método MoveTo**](moveto-method.md) para colocar el carácter en una nueva ubicación. Al llamar al **método MoveTo,** Microsoft Agent reproduce automáticamente la animación adecuada en función de la ubicación actual del carácter y, a continuación, mueve el marco del carácter. Del mismo modo, cuando se llama a [**GestureAt,**](gestureat-method.md)Microsoft Agent reproduce la animación de gestura adecuada en función de la ubicación del carácter y la ubicación especificada en la llamada.

Para ocultar el carácter, llame al [método Hide.](hide-method.md) Esto reproduce automáticamente el carácter asociado al estado **Ocultar** del carácter y, a continuación, oculta el marco del carácter. Sin embargo, también puede ocultar o mostrar un carácter estableciendo la propiedad [**Visible del**](visible-property.md) carácter.

Microsoft Agent procesa todas las llamadas de animación, *o solicitudes,* de forma asincrónica. Esto permite que el código de la aplicación siga controlando otros eventos mientras se procesa la solicitud. Por ejemplo, las llamadas al [**método Play**](play-method.md) coloca la animación en una cola para el carácter de modo que las animaciones se puedan reproducir secuencialmente. Sin embargo, esto significa que no se puede suponer que una llamada a otras funciones se ejecutará necesariamente después de una animación que sigue en el código. Por ejemplo, normalmente, una instrucción que sigue a una llamada a **Play** o [**MoveTo**](moveto-method.md) se ejecutará antes de que finalice la animación.

Puede sincronizar el código con animaciones en la cola de un carácter mediante la creación de una referencia [](the-request-object.md) de objeto a la solicitud de animación y, cuando la animación se inicia o completa, supervisa los eventos de solicitud que el servidor usa para notificar a los clientes del carácter. Por ejemplo, si desea que aparezca un cuadro de mensaje cuando el carácter finalice una animación, puede colocar la llamada al cuadro de mensaje en la subrutina de control de eventos [**RequestComplete,**](requestcomplete-event.md) comprobando el identificador de solicitud determinado.

Cuando un carácter está oculto, el servidor no reproduce animaciones; sin embargo, sigue en cola y procesa la solicitud de animación (reproduce la animación) y pasa un estado de solicitud al cliente. En el estado oculto, el carácter no puede convertirse en activo de entrada. Sin embargo, si el usuario habla el nombre del carácter (cuando la entrada de voz está habilitada), el servidor muestra automáticamente el carácter.

Cuando la aplicación cliente carga varios caracteres al mismo tiempo, los servicios de animación de Microsoft Agent permiten animar caracteres de forma independiente o usar los métodos [**Wait,**](wait-method.md) [**Interrupt**](interrupt-method.md)o [**Stop**](stop-method.md) para sincronizar su animación entre sí.

Microsoft Agent también reproduce automáticamente otras animaciones. Por ejemplo, si el estado del carácter no ha cambiado durante varios segundos, el Agente comienza a reproducir animaciones asignadas a las animaciones **de idling** del carácter. De forma similar, cuando la entrada de  voz está habilitada, el Agente reproduce las animaciones de escucha del carácter y, a continuación, las animaciones de escucha cuando se detecta una expresión.  Estas animaciones administradas por el servidor se *denominan estados* y se definen cuando se crea un carácter. Para obtener más información, [vea Designing Characters for Microsoft Agent](agent-states.md).

 

 