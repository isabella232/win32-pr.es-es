---
title: El objeto de solicitud
description: El objeto de solicitud
ms.assetid: d8b37164-6855-48c0-bcf8-a86c0f8b3a59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a50d554a5799af9a434b456113d7c826d2a0aa2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105704943"
---
# <a name="the-request-object"></a>El objeto de solicitud

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El servidor procesa algunos métodos de forma asincrónica. Esto permite que el código de la aplicación continúe mientras el método se está completando. Cuando una aplicación cliente llama a uno de estos métodos, el control crea y devuelve un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) para la solicitud. Puede usar el objeto de **solicitud** para realizar el seguimiento del estado del método mediante la asignación de una variable de objeto al método. En Visual Basic, en primer lugar, declare una variable de objeto:


```
   Dim MyRequest as Object
```



En VBScript, no se incluye el tipo de variable en la declaración:


```
   Dim MyRequest
```



Y use la instrucción set de Visual Basic para asignar la variable a la llamada al método:


```
   Set MyRequest = <i>agent</i>.Characters("<i>CharacterID</i>").<i>method</i> (<i>parameter</i>[s])
```



Esto agrega una referencia al objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) . El objeto de **solicitud** se destruirá cuando no haya más referencias a él. El punto en el que se declara el objeto de **solicitud** y cómo se usa determina su duración. Si el objeto se declara local a una subrutina o función, se destruirá cuando salga del ámbito; es decir, cuando finaliza la subrutina o la función. Si el objeto se declara globalmente, no se destruirá hasta que el programa finalice o hasta que se asigne un valor nuevo (o un valor establecido en "Empty") al objeto.

El objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) proporciona varias propiedades que se pueden consultar. Por ejemplo, la propiedad [**status**](status-property.md) devuelve el estado actual de la solicitud. Puede usar esta propiedad para comprobar el estado de la solicitud:


```
   Dim MyRequest
   
   Set MyRequest = Agent1.Characters.Load ("Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf")

   If (MyRequest.Status = 2) then
      'do something

   Else If (MyRequest.Status = 0) then
      'do something right away

   End If
```



La propiedad [**status**](status-property.md) devuelve el estado de un objeto [**request**](/windows/desktop/lwef/the-request-object) como un valor entero largo.



| Status | Definición                                        |
|--------|---------------------------------------------------|
| 0      | La solicitud se completó correctamente.                   |
| 1      | Error en la solicitud.                                   |
| 2      | Solicitud pendiente (en la cola, pero no completada). |
| 3      | Solicitud interrumpida.                              |
| 4      | Solicitud en curso.                              |



 

El objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) también incluye un valor entero largo en la propiedad [**Number**](https://www.bing.com/search?q=**Number**) que devuelve el error o la causa del código de [**Estado**](status-property.md) . Si no hay ninguno, este valor es cero (0). La propiedad [**Description**](description-property.md) contiene un valor de cadena que corresponde al número de error. Si la cadena no existe, la **Descripción** contiene "error definido por la aplicación o por el objeto".

Para obtener los valores y el significado devueltos por la propiedad [**Number**](https://www.bing.com/search?q=**Number**) , vea [códigos de error](microsoft-agent-error-codes.md).

El servidor coloca las solicitudes de animación en la cola del carácter especificado. Esto permite al servidor reproducir la animación en un subproceso independiente y el código de la aplicación puede continuar mientras se reproducen las animaciones. Si crea una referencia a un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) , el servidor le notificará automáticamente cuando se haya iniciado o completado una solicitud de animación a través de los eventos [**RequestStart**](https://www.bing.com/search?q=**RequestStart**) y [**RequestComplete**](https://www.bing.com/search?q=**RequestComplete**) . Dado que los métodos que devuelven objetos de **solicitud** son asincrónicos y puede que no se completen durante el ámbito de la función de llamada, declare la referencia al objeto de **solicitud** globalmente.

Los métodos siguientes se pueden usar para devolver un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) : [**GestureAt**](gestureat-method.md), [**Get**](get-method.md), [**Hide**](hide-method.md), [**Interrupt**](interrupt-method.md), [**Load**](load-method.md), [**moveTo**](moveto-method.md), [**Play**](play-method.md), [**Show**](show-method.md), [**Speak**](speak-method.md)y [**Wait**](https://www.bing.com/search?q=**Wait**).

 

 