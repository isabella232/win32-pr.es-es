---
title: Atributo ColorMode de VML
description: Atributo ColorMode de VML
ms.assetid: 92c885ca-7912-42ff-8f07-e6e779e0ef05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81b9b8699ac4806d47581f166dace38f8f724b015b25d18807caa48b44b283e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602146"
---
# <a name="vml-colormode-attribute"></a>Atributo ColorMode de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina el modo de color de extrusión. Lectura/escritura **DvTriState**.

**Se aplica a**

[Extrusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: *element* colormode=" *expression* ">

**Sintaxis de script**

*element* .colormode="*expression*"

*expresión* = *elemento*.colormode

**Comentarios:**

Estos valores incluyen:



| Value  | Descripción                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------|
| auto   | Especifica que el color de la extrusión es el mismo que el color de relleno de la forma. Predeterminada.                |
| custom | Especifica que la extrusión será el color del [atributo Color.](color-attribute--extrusion--vml.md) |



 

*Microsoft Office Atributo Extensions*

 

 