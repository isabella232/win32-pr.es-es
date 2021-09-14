---
title: Evento RequestComplete
description: Evento RequestComplete
ms.assetid: 543b79d1-f09d-4061-a1a8-8c8ab496bceb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 551aecdcfbeab76ab45e6211affef794ff37d876
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168222"
---
# <a name="requestcomplete-event"></a>Evento RequestComplete

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando el servidor completa una solicitud en cola.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Sub** *agent: \_ RequestComplete* *  **(ByVal** *Request):)**



| Parte      | Descripción                                            |
|-----------|--------------------------------------------------------|
| *Solicitud* | Devuelve el [**objeto Request.**](/windows/desktop/lwef/the-request-object) |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Este evento devuelve un [**objeto Request.**](/windows/desktop/lwef/the-request-object) Dado que las solicitudes se procesan de forma asincrónica, puede usar este evento para determinar cuándo el servidor finaliza el procesamiento de una solicitud (por ejemplo, un método [**Get**](get-method.md), [**Play**](play-method.md)o [**Speak)**](speak-method.md) para sincronizar este evento con otras acciones generadas por la aplicación. El servidor envía el evento solo al cliente que creó la referencia al objeto **Request** y solo si definió una variable global para la referencia de solicitud:


```
   Dim MyRequest 
   Dim Genie 

   Sub window_Onload
   
   Agent1.Characters.Load "Genie","https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent.Characters("Genie")

   ' This syntax will generate RequestStart and RequestComplete events.
   Set MyRequest = Genie.Get("state", "Showing")
   ' This syntax will not generate RequestStart and RequestComplete events.
   Genie.Get "state", "Hiding"
   
   End Sub

   Sub Agent1_RequestComplete(ByVal Request)

   If Request = MyRequest Then
      Status = "Showing animation is now loaded"

   End Sub
```



Dado que [**los objetos request**](/windows/desktop/lwef/the-request-object) de animación no se asignan hasta que el servidor procesa la solicitud, asegúrese de que el objeto **Request** existe antes de intentar evaluarlo. Por ejemplo, en Visual Basic, si usa un condicional para probar si se completó una solicitud específica, puede usar la palabra clave **Nothing:**


```
   Sub Agent1_RequestComplete (ByVal Request)

   If Not (MyRequest Is Nothing) Then
      If Request = MyRequest Then
      '-- Do whatever
      End If
   End If

   End Sub
```



> [!Note]  
> En VBScript 1.0, este evento se produce incluso si no se definen referencias a un [**objeto Request.**](/windows/desktop/lwef/the-request-object) Esto se ha corregido en VBScript 2.0, que se puede descargar desde <https://microsoft.com/msdownload/vbscript/scripting.asp> .

 

### <a name="see-also"></a>Consulte también

[**Evento RequestStart**](requeststart-event.md)


 

 