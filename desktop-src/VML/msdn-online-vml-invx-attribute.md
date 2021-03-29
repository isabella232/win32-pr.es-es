---
title: Atributo InvX de VML
description: Atributo InvX de VML
ms.assetid: 59fbd4c0-ae31-4198-a9e7-be12cd50288f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d244b5feff319112959d3093927f11d1e92164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792207"
---
# <a name="vml-invx-attribute"></a>Atributo InvX de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si se invierte la posición x del identificador. Lectura/escritura **VgTriState**.

**Se aplica a**

[H](msdn-online-vml-h-element.md) (subelemento de [Handles](msdn-online-vml-handles-element.md))

**Sintaxis de etiquetas**

<v: *Element* INVX = " *expresión* " >

**Comentarios:**

Si es **true**, la posición x del identificador se invierte restando el valor x del valor x de **CoordOrigin** agregado al valor x de **CoordSize**. El valor predeterminado es **False**.

Este atributo es el equivalente de

coordorigin. x + coordsize. x-h. position. x

*Atributo estándar de VML*

 

 