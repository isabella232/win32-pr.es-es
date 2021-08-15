---
title: Atributo ViewpointOrigin de VML
description: Atributo ViewpointOrigin de VML
ms.assetid: 4ccb3e12-bae4-4cb2-b48b-80c155ae7e03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5e69357eddfe535b3c6164579454260d8f478430f7a9f1c7bede3262b1b040
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007565"
---
# <a name="vml-viewpointorigin-attribute"></a>Atributo ViewpointOrigin de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el origen del punto de vista dentro del cuadro de límite de la forma. Lectura/escritura **Dvvector2D**.

**Se aplica a**

[Extrusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: *element* viewpointorigin=" *expression* ">

**Sintaxis de script**

*element* .viewpointorigin="*expression*"

*expresión* = *elemento*.viewpointorigin

**Comentarios:**

Define el punto de vista en términos de los valores x e y de la forma original. Los valores x e y oscilan entre 0,5 y -0,5 (del 50 % al -50 % del origen de coordenadas de la forma). El valor predeterminado es 0,0.

*Microsoft Office Atributo Extensions*

 

 