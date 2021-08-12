---
title: Atributo INVY de VML
description: Atributo INVY de VML
ms.assetid: 6c8c51ab-88ce-40b2-add7-1152e125ad8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d012e8ac6afe0e7808236c36d8dd3088ce9fa3552b4b7efa0542ea8612e4d36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599873"
---
# <a name="vml-invy-attribute"></a>Atributo INVY de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si se invierte la posición y del identificador. Lectura/escritura **DvTriState**.

**Se aplica a**

[H](msdn-online-vml-h-element.md) (subelemento de [identificadores)](msdn-online-vml-handles-element.md)

**Sintaxis de etiquetas**

<v: *element* invy=" *expression* ">

**Comentarios:**

Si **es True**, la posición y del identificador se invierte restando el valor y del valor y de **CoordOrigin** agregado al valor y de **CoordSize**. El valor predeterminado es **False**.

Este atributo es el equivalente de


```HTML
coordorigin.y + coordsize.y - h.position.y
```



*Atributo estándar de VML*

 

 