---
title: Elemento de grupo VML
description: Elemento de grupo VML
ms.assetid: 536c2380-2583-4fe8-a92e-c539de209a70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c128fddb5f070c9dbb6bbbd92c172cd58f5bce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420872"
---
# <a name="vml-group-element"></a>Elemento de grupo VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define un grupo que se puede usar para recopilar formas.

Este elemento admite los mismos atributos que una forma, excepto los siguientes:

-   **plusvalía**
-   **type**
-   **ajustar**
-   **path**
-   **spid**
-   **opacidad**
-   **chromakey**
-   **traza**
-   **strokecolor**
-   **strokeweight**
-   **Has**
-   **relleno**
-   **corta**
-   **ruleinitiator**
-   **ruleproxy**
-   **connectortype**
-   **bwmode**
-   **bwpure**
-   **bwnormal**
-   **forcedash**
-   **oleicon**
-   **preferrelative**
-   **OLE**

Solo se pueden usar los siguientes subelementos con **Group**.

-   **Grupo**
-   **TipoForma**
-   **Forma**
-   **Bloquear**

**Ejemplo**

En el ejemplo siguiente se muestra cómo definir un grupo.


```HTML
<!-- Include the VML behavior -->
<style>v\: * { behavior: url(#default#VML);display:inline-block }</style>

<!-- Declare the VML namespace -->
<xml:namespace ns="urn:schemas-microsoft-com:vml" prefix="v"/>

<v:group id="group1" style="left:10px;top:10px;width:50px;height:50px;"
  coordorigin="0,0" coordsize="6000,6000">

<v:shape id="_x0000_s2051"
  style='position:relative;left:234.75pt;top:208.875pt;width:235.25pt;height:128.875pt'
  coordsize="3765,2060"
  path="m1285,251l1126,469,580,1009,,1285,25,1412,93,1547,194,1673,1017,2026,2312,2060,3209,1756,3765,1388,3278,680,3059,319,2976,,1285,251,1285,251xe"
  fillcolor="#bcbcd6" stroked="f">
  <v:path arrowok="t"/>
 </v:shape>

 <v:shape id="_x0000_s2052" style='position:relative;left:314.625pt;
  top:140.5pt;width:104pt;height:102pt' coordsize="1663,1633"
  path="m0,1355l177,1498,353,1582,840,1633,1378,1498,1663,1295,1545,456,1260,10,1025,,656,260,253,874,,1355,,1355xe"
  fillcolor="#99ebff" stroked="f">
  <v:path arrowok="t"/>
 </v:shape>

</v:group>
```





 

 