---
title: Elemento Locks de VML
description: Elemento Locks de VML
ms.assetid: 1dfdc23a-0ad1-468f-a850-2068f3cc1803
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 258ad050ea59427e43faba5b92ddc93dfd62e5065c874a0c5f5d25d88e30fecc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573985"
---
# <a name="vml-locks-element"></a>Elemento Locks de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define un bloqueo para una forma.

Los atributos siguientes modifican un bloqueo.



| Atributo                                                    | Descripción                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------|
| [AdjustHandles](msdn-online-vml-adjusthandles-attribute.md) | Determina si se pueden editar los identificadores de una forma.                    |
| [AspectRatio](msdn-online-vml-aspectratio-attribute.md)     | Determina si un editor puede cambiar la relación de aspecto de una forma. |
| [Recorte](msdn-online-vml-cropping-attribute.md)           | Determina si se permitirá el recorte en un editor.                   |
| [Ext](ext-attribute--lock--vml.md)                          | Define el comportamiento de las acciones de bloqueo para un editor gráfico.             |
| [Agrupación](msdn-online-vml-grouping-attribute.md)           | Determina si las formas se pueden agrupar en un editor.                      |
| [Position](position-attribute--lock--vml.md)                | Determina si la posición de una forma está bloqueada en un editor.          |
| [Rotación](rotation-attribute--lock--vml.md)                | Determina si se permitirá la rotación de formas en un editor.         |
| [Selección](msdn-online-vml-selection-attribute.md)         | Determina si la forma se puede seleccionar en un editor.                    |
| [ShapeType](msdn-online-vml-shapetype-attribute.md)         | Determina si un editor puede cambiar el tipo AutoShapes.         |
| [Texto](msdn-online-vml-text-attribute.md)                   | Determina si se puede editar el texto adjunto a una forma.              |
| [Vértices](msdn-online-vml-vertices-attribute.md)           | Determina si un editor puede cambiar los vértices de una ruta de acceso.      |



 

**Comentarios:**

Este elemento debe definirse dentro de un [elemento Shape.](shape-element--vml.md)

El **elemento Locks** es una extensión Microsoft Office a VML.

 

 