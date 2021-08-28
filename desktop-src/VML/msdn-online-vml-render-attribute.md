---
title: Atributo de representación de VML
description: Atributo de representación de VML
ms.assetid: a05e7f6e-4784-4ff8-9deb-0501d3a5658e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17063d1e742a5b014e18d61d2d4290eb2511843ef24f1513bd3564ee83c5e4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513345"
---
# <a name="vml-render-attribute"></a>Atributo de representación de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el modo de representación de la extrusión. Lectura/escritura **Cadena**.

**Se aplica a**

[Extrusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: *element* render=" *expression* ">

**Sintaxis de script**

*element* .render="*expression*"

*expresión* = *elemento*.render

**Comentarios:**

Estos valores incluyen:



| Value        | Descripción                                                   |
|--------------|---------------------------------------------------------------|
| Sólido        | La representación muestra una forma sólida. Predeterminada.                    |
| Alambre    | La representación muestra una forma de wireframe.                         |
| boundingcube | La representación muestra el cubo delimitador que contiene la forma. |



 

*Microsoft Office Atributo Extensions*

 

 