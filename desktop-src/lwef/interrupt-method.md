---
title: Interrupt (método)
description: Interrupt (método)
ms.assetid: b8442e25-a629-47c7-acdd-1d28e74d78a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e66814963bb3de3db95d60cbc25777244626168e95ceee4bd3d8d76992dd72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749262"
---
# <a name="interrupt-method"></a>Interrupt (método)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Interrumpe la animación del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Solicitud de_ *  *interrupción*



| Parte      | Descripción                                                                  |
|-----------|------------------------------------------------------------------------------|
| *Solicitud* | Objeto [**Request**](/windows/desktop/lwef/the-request-object) para una llamada de animación determinada. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede usarlo para sincronizar la animación entre caracteres. Por ejemplo, si otro carácter está en una animación de bucle, este método detendrá el bucle y pasará a la animación siguiente de la cola del carácter. No puede interrumpir una animación de caracteres que no esté usando (que no haya cargado).

Para especificar el parámetro de solicitud, debe crear una variable y asignar la solicitud de animación que desea interrumpir:


```
   Dim GenieRequest as Object
   Dim RobbyRequest as Object
   Dim Genie as Object
   Dim Robby as Object

   Sub FormLoad()

      MyAgent1.Characters.Load "Genie", "Genie.acs"

      MyAgent1.Characters.Load "Robby", "Robby.acs"

      Set Genie = MyAgent1.Characters ("Genie")
      Set Robby = MyAgent1.Characters ("Robby")

      Genie.Show

      Genie.Speak "Just a moment"

      Set GenieRequest = Genie.Play ("Processing")

      Robby.Show
      Robby.Play "confused"
      Robby.Speak "Hey, Genie. What are you doing?"
      Robby.Interrupt GenieRequest

      Genie.Speak "I was just checking on something."

   End Sub
```



No se puede interrumpir la animación del mismo carácter que se especifica en este método porque el servidor pone en cola el método **Interrupt** en la cola de animación de ese carácter. Por lo tanto, solo puede usar **Interrumpir para** detener la animación de otro carácter que haya cargado.

Si declara una referencia de objeto y la establece en este método, devuelve un [**objeto Request.**](/windows/desktop/lwef/the-request-object)

> [!Note]  
> **La** interrupción no vacía la cola del carácter; detiene la animación existente y pasa a la animación siguiente en la cola del carácter. Para detener y vaciar la cola de un carácter, use el [**método Stop.**](stop-method.md)

 

## <a name="see-also"></a>Consulte también

[**Método Stop**](stop-method.md)


 

 