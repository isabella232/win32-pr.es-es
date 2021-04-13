---
title: Usar VBScript
description: Usar VBScript
ms.assetid: a078eb60-aa12-42ea-850c-7b845fc8037c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691ed6bf520c83e4b679bb174274abb984eaa2f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268903"
---
# <a name="using-vbscript"></a>Usar VBScript

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

VBScript es un lenguaje de programación incluido en Microsoft Internet Explorer. Para otros exploradores, póngase en contacto con el proveedor para obtener soporte técnico. Se recomienda el uso de VBScript 2,0 (o posterior) con el agente. Aunque las versiones anteriores de VBScript pueden funcionar con el agente, carecen de ciertas funciones que es posible que quiera usar. Puede descargar VBScript 2,0 y obtener más información sobre VBScript en el sitio de descargas de Microsoft y en el sitio de Microsoft VBScript.

Para programar Microsoft Agent desde VBScript, use el código HTML <SCRIPT> tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:

``` syntax
agent[.object].Method parameter, [parameter]
agent[.object].Property = value
```

En el caso de los eventos, incluya el nombre del control seguido del nombre del evento y cualquier parámetro:

``` syntax
Sub agent_event (ByVal parameter[,ByVal parameter])
statements
End Sub
```

También puede especificar un controlador de eventos mediante el <SCRIPT> tag's **For...Event** syntax:

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

Aunque Microsoft Internet Explorer es compatible con esta última sintaxis, no todos los exploradores. Por compatibilidad, use solo la sintaxis anterior para los eventos.

Con VBScript (2,0 o posterior), puede comprobar si el agente de Microsoft está instalado intentando crear el objeto y comprobando si existe. En el ejemplo siguiente se muestra cómo comprobar el control de agente sin desencadenar una descarga automática del control (como sucedería si incluyó una <OBJECT> etiqueta para el control en la página):

``` syntax
<!-- WARNING - This code requires VBScript 2.0.
It will always fail to detect the Agent control
in VbScript 1.x, because CreateObject doesn't work.
-->

<SCRIPT LANGUAGE=VBSCRIPT>
If HaveAgent() Then
      'Microsoft Agent control was found.
document.write "<H2 align=center>Found</H2>"
Else
      'Microsoft Agent control was not found.
document.write "<H2 align=center>Not Found</H2>"
End If

Function HaveAgent()
' This procedure attempts to create an Agent Control object.
' If it succeeds, it returns True.
'    This means the control is available on the client.
' If it fails, it returns False.
'    This means the control hasn't been installed on the client.

   Dim agent
   HaveAgent = False
   On Error Resume Next
   Set agent = CreateObject("Agent.Control.1")
   HaveAgent = IsObject(agent)

End Function

</SCRIPT>
```

 

 




