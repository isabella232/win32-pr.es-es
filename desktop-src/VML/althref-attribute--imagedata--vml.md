---
title: Atributo AltHRef (ImageData) (VML)
description: Atributo AltHRef (ImageData) (VML)
ms.assetid: c55ede90-3d57-4f27-9940-1fe4751cef71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 004625d769c12e67de024bf537ee04c377a18c8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077938"
---
# <a name="althref-attribute-imagedatavml"></a>Atributo AltHRef (ImageData) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Especifica una referencia alternativa para una imagen. Lectura/escritura **Cadena**.

**Se aplica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxis de etiquetas**

<v: *Element* o:althref = " *expresión* " >

**Sintaxis de script**

*Element* . althref = "*expresión*"

*expresión* = de *elemento*. althref

**Comentarios:**

Admite la conservación de datos PICT a través de Roundtripping HTML. En la escritura en HTML, se guarda la representación alternativa (es decir, los datos PICT originales si el archivo se originó en el equipo Macintosh). En una lectura de HTML, **AltHRef** se favorece en **src**.

*Microsoft Office atributo Extensions*

 

 