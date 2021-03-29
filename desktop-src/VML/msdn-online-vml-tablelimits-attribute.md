---
title: Atributo TableLimits de VML
description: Atributo TableLimits de VML
ms.assetid: eef855de-23c5-4894-b7cf-2ea39e372e08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b35a7449cc2f348e6040161c1fb599c29972803
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791835"
---
# <a name="vml-tablelimits-attribute"></a>Atributo TableLimits de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Lista de valores de alto mínimo para cada fila de una tabla. Lectura/escritura **VgLengthArray**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* o:tablelimits = " *expresión* " >

**Comentarios:**

Usado por Microsoft PowerPoint para tablas nativas. El valor predeterminado es **null**.

Aunque el valor se almacena en una forma, el atributo solo es útil cuando la tabla está formada por formas agrupadas. Cuando se agrega texto a las celdas de la tabla, puede aumentar el alto de la fila. El atributo **TableLimits** almacena el alto de la fila original para que, si se elimina el texto, el alto de la fila no se sitúe por debajo del valor original.

*Microsoft Office atributo Extensions*

 

 