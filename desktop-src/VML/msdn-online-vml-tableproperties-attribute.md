---
title: Atributo TableProperties de VML
description: Atributo TableProperties de VML
ms.assetid: 10355742-13b9-4c08-bff7-f7f7501762e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050e290bc4b779fec40ebf3ad3fb202b34af23b10f70a0070038c56f5f8ea2c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597551"
---
# <a name="vml-tableproperties-attribute"></a>Atributo TableProperties de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina las propiedades de la tabla. Lectura/escritura **Entero**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *elemento* o:tableproperties=" *expresión* ">

**Comentarios:**

Usado por Microsoft PowerPoint para tablas nativas. El valor predeterminado es 0. Solo se usan los tres primeros bits de este entero.

Aunque el valor se almacena en una forma, el atributo solo es útil cuando la tabla está creada con formas agrupadas. Los bits se pueden combinar.

Se incluyen los siguientes valores de bits.



| bit | Descripción                              |
|-----|------------------------------------------|
| 1   | Establezca si el grupo de formas es una tabla.   |
| 2   | Establezca si la forma es un marcador de posición.       |
| 3   | Establezca si el texto de la tabla es bidireccional. |



 

*Microsoft Office Atributo Extensions*

 

 