---
title: Uso del monitor de sistema
description: El monitor de sistema (SYSMON) puede incluirse en cualquier aplicación que admita ActiveX \ 174; permite. Por ejemplo, puede incluir SYSMON en una aplicación de Microsoft Visual Basic o en un documento HTML.
ms.assetid: 36931aae-b608-42d9-a3e3-09784e80f386
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abd636c8b984f7c891c2222b4674dd8d0d7e747d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665679"
---
# <a name="using-system-monitor"></a>Uso del monitor de sistema

El monitor de sistema (SYSMON) puede incluirse en cualquier aplicación que admita controles de® ActiveX. Por ejemplo, puede incluir SYSMON en una aplicación de Microsoft Visual Basic o en un documento HTML.

En el ejemplo siguiente se muestra cómo incluir SYSMON en un documento HTML. En el ejemplo se usa VBScript para agregar contadores cuyos valores se recuperan del equipo local, se modifican algunas de las propiedades de SYSMON que controlan cómo se muestra el monitor y se procesa el evento OnCounterAdd. En el ejemplo se usa el carácter comodín ( \* ) para agregar todas las instancias del contador de procesos.

``` syntax
<HTML>
<BODY BGCOLOR=#C0C0C0>

<SCRIPT LANGUAGE="VBScript">
  Sub Monitor_OnCounterAdded(index)
    Monitor.Counters.Item(1).Width = 8
  End Sub
</Script>
<OBJECT
  CLASSID="clsid:C4D2D8E0-D1DD-11CE-940F-008029004347"
  ID="Monitor"
  HEIGHT=80%
  WIDTH=100%>
</OBJECT>

<SCRIPT LANGUAGE="VBScript">
  Sub Window_OnLoad
    On Error Resume Next
    Monitor.ShowValueBar = False
    Monitor.ShowHorizontalGrid = True
    Monitor.Counters.Add("\Process(*)\% Processor Time")
    Monitor.DisplayType=sysmonLineGraph
    Monitor.GraphTitle="System Performance Overview"
  End Sub
</SCRIPT>

</BODY>
</HTML>
```

 

 




