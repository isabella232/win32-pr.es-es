---
title: Control de errores (SDK de Windows Media Player)
description: Tratamiento de errores
ms.assetid: f0567c77-a855-4b93-9fb7-a36cde63859f
keywords:
- Windows Media Player, control de errores
- Modelo de objetos de Windows Media Player, control de errores
- modelo de objetos, control de errores
- Control ActiveX de Windows Media Player, control de errores
- Control ActiveX, control de errores
- Control ActiveX de Windows Media Player Mobile, control de errores
- Windows Media Player Mobile, control de errores
- Guía de migración, control de errores
- control de errores en el modelo de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3b96e04d24009ee4b7e5819fdb26dfd6effd63
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149766"
---
# <a name="error-handling-windows-media-player-sdk"></a>Control de errores (SDK de Windows Media Player)

El control ActiveX de Windows Media Player 6,4 proporciona un control de errores predeterminado al mostrar los mensajes de error en los cuadros de diálogo y en la barra de estado. También puede proporcionar un control de errores personalizado mediante el procesamiento de errores en el script. El control de errores se basa en eventos, lo que significa que recibe una notificación para cada error y debe decidir cómo tratar cada evento de error cuando se produce. Para obtener más información sobre el control de errores con el modelo de objetos de la versión 6,4, consulte la sección control de errores de la guía del modelo de objetos del reproductor de la versión 6,4, que forma parte del SDK de Windows Media Player.

El modelo de objetos de Windows Media Player 7 o posterior proporciona el objeto de **error** y el objeto **ErrorItem** para controlar los errores. Estos dos objetos funcionan juntos para proporcionar un mecanismo de control de errores que le proporciona un control completo y flexible del proceso de control de errores. El objeto **error** proporciona acceso a una colección de objetos **ErrorItem** ; cada objeto **ErrorItem** proporciona detalles sobre un mensaje de error individual.

Cuando se produce un error, la información de error se envía a una cola de errores. La cola es una colección de objetos **ErrorItem** . A medida que se agrega cada error a la cola, se asocia a un número de índice (a partir de cero) que se puede utilizar para identificar el objeto **ErrorItem** determinado. El *error*. la propiedad **errorCount** recupera el número de errores en la cola de errores. Dado que los números de índice son de base cero, el error más reciente expuesto en la cola siempre tendrá un valor de índice igual a *error*. **errorCount** menos uno.

Puede crear un controlador de eventos de error para Windows Media Player mediante un script. En el siguiente ejemplo de JScript se muestra cómo recuperar el elemento de error más reciente de la cola de errores y mostrar el código de error y la descripción del error mediante el modelo de objetos de Windows Media Player 7 o posterior. El objeto **Player** se creó con ID = "WMP9".


```C++
<!-- Create an error event handler for Windows Media Player 7 or later errors. -->
<SCRIPT  LANGUAGE = "JScript"  FOR = WMP9  EVENT = error()>

// Store the number of errors in the error queue.
var max = WMP9.error.errorCount;

// Retrieve most recent ErrorItem object.
var err = WMP9.error.item(max-1)

// Store the error code number.
var errNum = err.errorCode;

// Store the error description string.
var errDesc = err.errorDescription;

// Build a message string to notify the user.
var msg = "Error number: " + errNum + "\n";
msg += "Error description: " + errDesc;

// Display the message box.
alert(msg);

</SCRIPT>

```



El objeto de **error** tiene dos métodos adicionales que puede usar. El *error*. el método **clearErrorQueue** permite quitar todos los errores de la cola de errores y restablecer el número de índice en cero. Tiene un control total sobre este proceso; puede mantener los errores en la cola mientras necesite que estén disponibles y, a continuación, vaciar la cola cuando haya terminado de controlar los errores.

El *error*. **WebHelp** Method proporciona una manera de mostrar la información de error más reciente al usuario mediante Internet. Cuando se llama, este método transfiere toda la información relevante sobre el primer error de la cola (el que tiene el índice cero) a la ayuda Web de Microsoft Windows Media Player, que muestra más información sobre el error en la ventana del explorador actual.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objeto de error**](error-object.md)
</dt> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> <dt>

[**Guía de migración del modelo de objetos**](object-model-migration-guide.md)
</dt> </dl>

 

 




