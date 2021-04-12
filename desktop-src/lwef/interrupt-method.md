---
title: Método Interrupt
description: Método Interrupt
ms.assetid: b8442e25-a629-47c7-acdd-1d28e74d78a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58050e181525cc4a4b9f35ec169e92d91ab28e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420720"
---
# <a name="interrupt-method"></a>Método Interrupt

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Interrumpe la animación del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID * *").* *  *Solicitud* de interrupción



| Parte      | Descripción                                                                  |
|-----------|------------------------------------------------------------------------------|
| *Solicitud* | Objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) para una llamada de animación determinada. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede utilizar esto para sincronizar la animación entre los caracteres. Por ejemplo, si hay otro carácter en una animación de bucle, este método detendrá el bucle y se desplazará a la siguiente animación de la cola del carácter. No se puede interrumpir una animación de caracteres que no se esté usando (que no se ha cargado).

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



No se puede interrumpir la animación del mismo carácter que se especifica en este método porque el servidor pone en cola el método de **interrupción** en la cola de animaciones de ese carácter. Por lo tanto, solo puede usar la **interrupción** para detener la animación de otro carácter que haya cargado.

Si declara una referencia de objeto y la establece en este método, devuelve un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .

> [!Note]  
> La **interrupción** no vacía la cola del carácter; detiene la animación existente y pasa a la siguiente animación de la cola del carácter. Para detener y vaciar la cola de un carácter, utilice el método [**Stop**](stop-method.md) .

 

## <a name="see-also"></a>Consulte también

[**Método Stop**](stop-method.md)


 

 