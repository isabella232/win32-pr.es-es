---
title: Uso de VBScript
description: Uso de VBScript
ms.assetid: a078eb60-aa12-42ea-850c-7b845fc8037c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0bc64419af4d8dc47de5a2393fcf5cb259374ed
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881012"
---
# <a name="using-vbscript"></a>Uso de VBScript

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

VBScript es un lenguaje de programación incluido con Microsoft Internet Explorer. Para otros exploradores, póngase en contacto con su proveedor para obtener soporte técnico. VbScript 2.0 (o posterior) se recomienda para su uso con el Agente . Aunque las versiones anteriores de VBScript pueden funcionar con el Agente , carecen de ciertas funciones que puede que quiera usar. Puede descargar VBScript 2.0 y obtener más información sobre VBScript en el sitio de descargas de Microsoft y el sitio de Microsoft VBScript.

Para programar Microsoft Agent desde VBScript, use las etiquetas &lt; HTML &gt; SCRIPT. Para acceder a la interfaz de programación, use el nombre del control que asigne en la etiqueta OBJECT, seguido del subobjeto (si lo hubiera), el nombre del método o la propiedad y los parámetros o valores admitidos por el método o la &lt; &gt; propiedad:

``` syntax
agent[.object].Method parameter, [parameter]
agent[.object].Property = value
```

Para los eventos, incluya el nombre del control seguido del nombre del evento y cualquier parámetro:

``` syntax
Sub agent_event (ByVal parameter[,ByVal parameter])
statements
End Sub
```

También puede especificar un controlador de eventos mediante la etiqueta &lt; &gt; SCRIPT **For... Sintaxis de** eventos:

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

Aunque Microsoft Internet Explorer admite esta última sintaxis, no todos los exploradores sí. Por compatibilidad, use solo la sintaxis anterior para los eventos.

Con VBScript (2.0 o posterior), puede comprobar si Microsoft Agent está instalado intentando crear el objeto y comprobando si existe. En el ejemplo siguiente se muestra cómo buscar el control agente sin desencadenar una descarga automática del control (como sucedería si incluyera una etiqueta OBJECT para el control en &lt; &gt; la página):

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

 

 




