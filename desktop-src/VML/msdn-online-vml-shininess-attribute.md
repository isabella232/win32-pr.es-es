---
title: Atributo VmLIness
description: Atributo VmLIness
ms.assetid: 99c301ff-ed61-48ef-95bb-ceaed1a2553c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dea0abba3f605f749e07d247d207a50a6fe7b247ec54bd88024bad3915285e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099055"
---
# <a name="vml-shininess-attribute"></a>Atributo VmLIness

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la concentración de la luz reflejada en una superficie de extrusión. Lectura/escritura **NumberNumber**.

**Se aplica a**

[Extrusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: *elementiness="* *expression* ">

**Sintaxis de script**

*element* .iness="*expression*"

*expresión* = *elemento*.iness

**Comentarios:**

Los valores altos (8-10) se aproximaban a la disponibilidad de un reflejo y los valores bajos (2-3) se aproximaban a un efecto de kled. Los valores de 4 a 7 son típicos. Las reflexión no reflejan otros objetos; solo se reflejan los orígenes de luz de identificar. El valor predeterminado es 5.

*Microsoft Office Atributo Extensions*

 

 