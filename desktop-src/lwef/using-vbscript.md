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
# <a name="using-vbscript"></a><span data-ttu-id="2135c-103">Usar VBScript</span><span class="sxs-lookup"><span data-stu-id="2135c-103">Using VBScript</span></span>

<span data-ttu-id="2135c-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2135c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="2135c-105">VBScript es un lenguaje de programación incluido en Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2135c-105">VBScript is a programming language included with Microsoft Internet Explorer.</span></span> <span data-ttu-id="2135c-106">Para otros exploradores, póngase en contacto con el proveedor para obtener soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="2135c-106">For other browsers, contact your vendor about support.</span></span> <span data-ttu-id="2135c-107">Se recomienda el uso de VBScript 2,0 (o posterior) con el agente.</span><span class="sxs-lookup"><span data-stu-id="2135c-107">VBScript 2.0 (or later) is recommended for use with Agent.</span></span> <span data-ttu-id="2135c-108">Aunque las versiones anteriores de VBScript pueden funcionar con el agente, carecen de ciertas funciones que es posible que quiera usar.</span><span class="sxs-lookup"><span data-stu-id="2135c-108">Although earlier versions of VBScript may work with Agent, they lack certain functions that you may want to use.</span></span> <span data-ttu-id="2135c-109">Puede descargar VBScript 2,0 y obtener más información sobre VBScript en el sitio de descargas de Microsoft y en el sitio de Microsoft VBScript.</span><span class="sxs-lookup"><span data-stu-id="2135c-109">You can download VBScript 2.0 and obtain further information on VBScript at the Microsoft Downloads site and the Microsoft VBScript site.</span></span>

<span data-ttu-id="2135c-110">Para programar Microsoft Agent desde VBScript, use el código HTML</span><span class="sxs-lookup"><span data-stu-id="2135c-110">To program Microsoft Agent from VBScript, use the HTML</span></span> <SCRIPT> <span data-ttu-id="2135c-111">tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:</span><span class="sxs-lookup"><span data-stu-id="2135c-111">tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:</span></span>

``` syntax
agent[.object].Method parameter, [parameter]
agent[.object].Property = value
```

<span data-ttu-id="2135c-112">En el caso de los eventos, incluya el nombre del control seguido del nombre del evento y cualquier parámetro:</span><span class="sxs-lookup"><span data-stu-id="2135c-112">For events, include the name of the control followed by the name of the event and any parameters:</span></span>

``` syntax
Sub agent_event (ByVal parameter[,ByVal parameter])
statements
End Sub
```

<span data-ttu-id="2135c-113">También puede especificar un controlador de eventos mediante el</span><span class="sxs-lookup"><span data-stu-id="2135c-113">You can also specify an event handler using the</span></span> <SCRIPT> <span data-ttu-id="2135c-114">tag's **For...Event** syntax:</span><span class="sxs-lookup"><span data-stu-id="2135c-114">tag's **For...Event** syntax:</span></span>

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

<span data-ttu-id="2135c-115">Aunque Microsoft Internet Explorer es compatible con esta última sintaxis, no todos los exploradores.</span><span class="sxs-lookup"><span data-stu-id="2135c-115">Although Microsoft Internet Explorer supports this latter syntax, not all browsers do.</span></span> <span data-ttu-id="2135c-116">Por compatibilidad, use solo la sintaxis anterior para los eventos.</span><span class="sxs-lookup"><span data-stu-id="2135c-116">For compatibility, use only the former syntax for events.</span></span>

<span data-ttu-id="2135c-117">Con VBScript (2,0 o posterior), puede comprobar si el agente de Microsoft está instalado intentando crear el objeto y comprobando si existe.</span><span class="sxs-lookup"><span data-stu-id="2135c-117">With VBScript (2.0 or later), you can verify whether Microsoft Agent is installed by trying to create the object and checking to see if it exists.</span></span> <span data-ttu-id="2135c-118">En el ejemplo siguiente se muestra cómo comprobar el control de agente sin desencadenar una descarga automática del control (como sucedería si incluyó una <OBJECT> etiqueta para el control en la página):</span><span class="sxs-lookup"><span data-stu-id="2135c-118">The following sample demonstrates how to check for the Agent control without triggering an auto-download of the control (as would happen if you included an <OBJECT> tag for the control on the page):</span></span>

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

 

 




