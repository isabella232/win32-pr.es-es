---
title: El objeto Request
description: El objeto Request
ms.assetid: d8b37164-6855-48c0-bcf8-a86c0f8b3a59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2bc9ecf65403ca6dbb471c81a65b105bcc5b69701760a73f8fbc8a5684a9b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117882398"
---
# <a name="the-request-object"></a>El objeto Request

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

El servidor procesa algunos métodos de forma asincrónica. Esto permite que el código de la aplicación continúe mientras se completa el método. Cuando una aplicación cliente llama a uno de estos métodos, el control crea y devuelve un [**objeto Request**](/windows/desktop/lwef/the-request-object) para la solicitud. Puede usar el **objeto Request** para realizar un seguimiento del estado del método mediante la asignación de una variable de objeto al método . En Visual Basic, declare primero una variable de objeto:


```
   Dim MyRequest as Object
```



En VBScript, no se incluye el tipo de variable en la declaración:


```
   Dim MyRequest
```



Y use Visual Basic instrucción Set para asignar la variable a la llamada al método:


```
   Set MyRequest = <i>agent</i>.Characters("<i>CharacterID</i>").<i>method</i> (<i>parameter</i>[s])
```



Esto agrega una referencia al [**objeto Request.**](/windows/desktop/lwef/the-request-object) El **objeto** Request se destruirá cuando no haya más referencias a él. El lugar en el que se **declara** el objeto Request y cómo se usa determina su duración. Si el objeto se declara local en una subrutina o función, se destruirá cuando salga del ámbito; es decir, cuando finaliza la subrutina o función. Si el objeto se declara globalmente, no se destruirá hasta que finalice el programa o se asigne un nuevo valor (o un valor establecido en "vacío") al objeto.

El [**objeto Request**](/windows/desktop/lwef/the-request-object) proporciona varias propiedades que puede consultar. Por ejemplo, la [**propiedad Status**](status-property.md) devuelve el estado actual de la solicitud. Puede usar esta propiedad para comprobar el estado de la solicitud:


```
   Dim MyRequest
   
   Set MyRequest = Agent1.Characters.Load ("Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf")

   If (MyRequest.Status = 2) then
      'do something

   Else If (MyRequest.Status = 0) then
      'do something right away

   End If
```



La [**propiedad Status**](status-property.md) devuelve el estado de un objeto [**Request**](/windows/desktop/lwef/the-request-object) como un valor entero Long.



| Status | Definición                                        |
|--------|---------------------------------------------------|
| 0      | Solicitud completada correctamente.                   |
| 1      | Error de solicitud.                                   |
| 2      | Solicitud pendiente (en la cola, pero no completa). |
| 3      | Solicitud interrumpida.                              |
| 4      | Solicitud en curso.                              |



 

El [**objeto Request**](/windows/desktop/lwef/the-request-object) también incluye un valor entero Long en la propiedad [**Number**](https://www.bing.com/search?q=**Number**) que devuelve el error o la causa del código [**de**](status-property.md) estado. Si no es ninguno, este valor es cero (0). La [**propiedad Description**](description-property.md) contiene un valor de cadena que corresponde al número de error. Si la cadena no existe, **Description** contiene "Error definido por la aplicación o definido por el objeto".

Para obtener los valores y el significado devueltos por [**la propiedad Number,**](https://www.bing.com/search?q=**Number**) vea [Códigos de error.](microsoft-agent-error-codes.md)

El servidor coloca las solicitudes de animación en la cola del carácter especificado. Esto permite al servidor reproducir la animación en un subproceso independiente y el código de la aplicación puede continuar mientras se reproducen las animaciones. Si crea una [**referencia**](/windows/desktop/lwef/the-request-object) de objeto Request, el servidor le notificará automáticamente cuando se haya iniciado o completado una solicitud de animación a través de los eventos [**RequestStart**](https://www.bing.com/search?q=**RequestStart**) [**y RequestComplete.**](https://www.bing.com/search?q=**RequestComplete**) Dado que los métodos que devuelven objetos **Request** son asincrónicos y pueden no completarse durante el ámbito de la función que realiza la llamada, declare la referencia al **objeto Request** globalmente.

Los métodos siguientes se [](/windows/desktop/lwef/the-request-object) pueden usar para devolver un objeto Request: [**GestureAt**](gestureat-method.md), [**Get**](get-method.md), [**Hide**](hide-method.md), [**Interrupt**](interrupt-method.md), [**Load**](load-method.md), [**MoveTo**](moveto-method.md), [**Play**](play-method.md), [**Show**](show-method.md), [**Speak**](speak-method.md)y [**Wait**](https://www.bing.com/search?q=**Wait**).

 

 