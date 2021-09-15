---
title: Evento RequestStart
description: Evento RequestStart
ms.assetid: ecfb9691-cbc4-48f5-8e26-a99389e85eed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2be5954636084d3cbc299c718f2b4e6d9330ef90
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568709"
---
# <a name="requeststart-event"></a>Evento RequestStart

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando el servidor inicia una solicitud en cola.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Sub** *agent** \_ RequestStart* *  **(ByVal** *Request):)**



| Parte      | Descripción                                            |
|-----------|--------------------------------------------------------|
| *Solicitud* | Devuelve el [**objeto Request.**](/windows/desktop/lwef/the-request-object) |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

El evento devuelve un [**objeto Request.**](/windows/desktop/lwef/the-request-object) Dado que las solicitudes se procesan de forma asincrónica, puede usar este evento para determinar cuándo el servidor comienza a procesar una solicitud (por ejemplo, un método [**Get**](get-method.md), [**Play**](play-method.md)o [**Speak)**](speak-method.md) y, por tanto, sincronizarla con otras acciones generadas por la aplicación. El evento solo se envía al cliente que creó la referencia al objeto **Request** y solo si definió una variable global para la referencia de solicitud:


```
   Dim MyRequest 
   Dim Genie 

   Sub window_Onload
   
   Agent1.Characters.Load "Genie", _
      "https://agent.microsoft.com/characters/v2/genie/genie.acf"   

   Set Genie = Agent1.Characters("Genie")

   ' This syntax will generate RequestStart and RequestComplete events.
   Set MyRequest = Genie.Get("state", "Showing")

   ' This syntax will not generate RequestStart and RequestComplete events.
   Genie.Get ("state", "Hiding")

   End Sub

   Sub Agent1_RequestStart(ByVal Request)

   If Request = MyRequest Then
      Status = "Loading the Showing animation"

   End Sub
```



El [**estado**](status-property.md) devuelve 4 (solicitud en curso) para el [**objeto Request**](/windows/desktop/lwef/the-request-object) devuelto.

Dado que [**los objetos request**](/windows/desktop/lwef/the-request-object) de animación no se asignan hasta que el servidor procesa la solicitud, asegúrese de que el objeto **Request** existe antes de intentar evaluarlo. Por ejemplo, en Visual Basic, si usa un condicional para probar si se completó una solicitud específica, puede usar la palabra clave **Nothing:**


```
   Sub Agent1_RequestStart (ByVal Request)

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

[**Evento RequestComplete**](requestcomplete-event.md)


 

 