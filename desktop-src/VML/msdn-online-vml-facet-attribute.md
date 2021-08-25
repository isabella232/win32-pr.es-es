---
title: Atributo de faceta de VML
description: Atributo de faceta de VML
ms.assetid: 6b874d79-a34e-45f7-bbbf-44d652410b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b1ae12ba31d286f1e029dcd433820e8c50acb05c86a92b2c06e1df50c73a0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681015"
---
# <a name="vml-facet-attribute"></a>Atributo de faceta de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el número de facetas usadas para describir las superficies curvas de una extrusión. Lectura/escritura **Numbernumber .**

**Se aplica a**

[Extrusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: *element* facet=" *expression* ">

**Sintaxis de script**

*element* .facet="*expression*"

*expresión* = *elemento*.facet

**Comentarios:**

Define la manera en que un motor de representación se aproximará a la extrusión. Un número inferior indicará una tolerancia de representación inferior al motor de representación y dará lugar a más facetas. Los números más altos harán que la extrusión parezca más por caras. El valor predeterminado es 30 000.

*Microsoft Office Atributo Extensions*

 

 