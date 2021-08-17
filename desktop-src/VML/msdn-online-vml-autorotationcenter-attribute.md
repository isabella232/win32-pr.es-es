---
title: Atributo AutoRotationCenter de VML
description: Atributo AutoRotationCenter de VML
ms.assetid: beb6771f-42f4-458a-b525-4eb67bc1eff0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54b363b34a6b2f943be45d457e252eebcf597afd7f82b7992cf151b0c2eda4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118347107"
---
# <a name="vml-autorotationcenter-attribute"></a>Atributo AutoRotationCenter de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si el centro de rotación será el centro geométrico de la extrusión. Lectura/escritura **DvTriState**.

**Se aplica a**

[Extrusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: *element* autorotationcenter=" *expression* ">

**Sintaxis de script**

*element* .autorotationcenter="*expression*"

*expresión* = *elemento*.autorotationcenter

**Comentarios:**

El centro geométrico de una forma extruida es 0,0,0. Si el valor de este atributo es **False**, el centro de rotación viene determinado por el [atributo RotationCenter.](msdn-online-vml-rotationcenter-attribute.md) El valor predeterminado es **False**.

*Microsoft Office Atributo Extensions*

 

 