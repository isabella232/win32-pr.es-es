---
title: Elemento Locks de VML
description: Elemento Locks de VML
ms.assetid: 1dfdc23a-0ad1-468f-a850-2068f3cc1803
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a3d246e486d1b7db99484777355b9160b71b6b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149440"
---
# <a name="vml-locks-element"></a>Elemento Locks de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define un bloqueo para una forma.

Los atributos siguientes modifican un bloqueo.



| Atributo                                                    | Descripción                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------|
| [AdjustHandles](msdn-online-vml-adjusthandles-attribute.md) | Determina si se pueden editar los controladores de una forma.                    |
| [AspectRatio](msdn-online-vml-aspectratio-attribute.md)     | Determina si un editor puede cambiar la relación de aspecto de una forma. |
| [Recorte](msdn-online-vml-cropping-attribute.md)           | Determina si se permitirá el recorte en un editor.                   |
| [Total](ext-attribute--lock--vml.md)                          | Define el comportamiento de las acciones de bloqueo para un editor gráfico.             |
| [Agrupación](msdn-online-vml-grouping-attribute.md)           | Determina si las formas se pueden agrupar en un editor.                      |
| [Position](position-attribute--lock--vml.md)                | Determina si la posición de una forma está bloqueada en un editor.          |
| [Rotación](rotation-attribute--lock--vml.md)                | Determina si se permitirá la rotación de formas en un editor.         |
| [Selección](msdn-online-vml-selection-attribute.md)         | Determina si la forma se selecciona en un editor.                    |
| [TipoForma](msdn-online-vml-shapetype-attribute.md)         | Determina si un editor puede cambiar el tipo de autoformas.         |
| [Texto](msdn-online-vml-text-attribute.md)                   | Determina si se puede editar el texto asociado a una forma.              |
| [Vértices](msdn-online-vml-vertices-attribute.md)           | Determina si un editor puede cambiar los vértices de una ruta de acceso.      |



 

**Comentarios:**

Este elemento debe definirse dentro de un elemento de [forma](shape-element--vml.md) .

El elemento **Locks** es una extensión de Microsoft Office a VML.

 

 