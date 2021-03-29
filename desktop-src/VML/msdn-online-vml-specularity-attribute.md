---
title: Atributo de especulación VML
description: Atributo de especulación VML
ms.assetid: df04c15c-cfad-4172-81fa-a28e13f205fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b4e8814a9bd0cd897ae018cf8b37aa67d732aa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904689"
---
# <a name="vml-specularity-attribute"></a>Atributo de especulación VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define la especulación de una forma extruida. Lectura/escritura **VgNumber**.

**Se aplica a**

[Trusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: especular de *elemento* = " *expresión* " >

**Sintaxis de script**

*Element* . especulate = "*Expression*"

*expresión* = de *elemento*. especulate

**Comentarios:**

Este valor define la relación de la luz de incidente con la luz reflejada especular. Los valores normales oscilan entre 0 y 1. El valor predeterminado es 0.

Si se especifican valores mayores que 1, se pueden producir efectos inusuales.

Microsoft Office atributo Extensions

 

 