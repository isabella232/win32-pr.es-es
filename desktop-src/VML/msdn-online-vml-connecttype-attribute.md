---
title: Atributo ConnectType de VML
description: Atributo ConnectType de VML
ms.assetid: 907803c8-687b-4823-8252-b59acbbd9aa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76910977c0673500be2e91d9f387b1e61782a1460e5de0d513784caa6f0f1633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999265"
---
# <a name="vml-connecttype-attribute"></a>Atributo ConnectType de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el tipo de puntos de conexión usados para adjuntar formas a otras formas. Lectura/escritura **Cadena**.

**Se aplica a**

[Ruta de acceso](msdn-online-vml-path-element.md)

**Sintaxis de etiquetas**

<v: *element* o:connecttype=" *expression* ">

**Comentarios:**

Estos valores incluyen:



| Value    | Descripción                                                                                                                           |
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| ninguno     | No hay sitios de conexión. Predeterminada.                                                                                                         |
| rect     | Cuatro puntos de conexión estándar en puntos medios de los lados superior, inferior, izquierdo y derecho.                                                   |
| segmentos | Se usan los puntos de edición de la forma. Los puntos de edición son los puntos negros de un editor gráfico que se usan para seleccionar partes de una forma. |
| custom   | Matriz personalizada de ubicaciones de conexión.                                                                                               |



 

*Microsoft Office Atributo Extensions*

 

 