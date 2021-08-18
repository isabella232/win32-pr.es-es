---
title: Atributo clip de VML
description: Atributo clip de VML
ms.assetid: 8839c10e-96dd-4419-9f02-80033a4633e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cab4afdef2a10c9c6f6a0561dedf5b4df3538a97152cb53181452b8ac531bb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999295"
---
# <a name="vml-clip-attribute"></a>Atributo clip de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si el recorte está en. Lectura/escritura **DvTriState**.

**Se aplica a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintaxis de etiquetas**

<v: *element* clip=" *expression* ">

**Sintaxis de script**

*element* .clip="*expression*"

*expresión* = *elemento*.clip

**Comentarios:**

Si **Clip** es **False,** la forma se escalará para ajustarse al marco. Si **es True**, no se mostrarán las partes de la forma que estén fuera del marco.

Tenga en cuenta [que Origin](origin-attribute--vmlframe--vml.md) [y Size](size-attribute--vmlframe.md) no se usarán a menos **que Clip** sea **True.**

*Atributo estándar de VML*

**Ejemplo**

Se recortará la imagen definida en el archivo externo.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 