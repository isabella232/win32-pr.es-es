---
title: Atributo TableProperties de VML
description: Atributo TableProperties de VML
ms.assetid: 10355742-13b9-4c08-bff7-f7f7501762e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f0f010f673b2663764814150f7a38fc06f23e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695610"
---
# <a name="vml-tableproperties-attribute"></a>Atributo TableProperties de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina las propiedades de la tabla. Lectura/escritura **Entero**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *Element* o:TableProperties = " *expresión* " >

**Comentarios:**

Usado por Microsoft PowerPoint para tablas nativas. El valor predeterminado es 0. Solo se utilizan los tres primeros bits de este entero.

Aunque el valor se almacena en una forma, el atributo solo es útil cuando la tabla está formada por formas agrupadas. Se pueden combinar bits.

Se incluyen los siguientes valores de bit.



| bit | Descripción                              |
|-----|------------------------------------------|
| 1   | Se establece si el grupo de formas es una tabla.   |
| 2   | Se establece si la forma es un marcador de posición.       |
| 3   | Se establece si el texto de la tabla es bidireccional. |



 

*Microsoft Office atributo Extensions*

 

 