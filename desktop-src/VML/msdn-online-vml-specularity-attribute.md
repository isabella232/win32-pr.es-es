---
title: Atributo specularity de VML
description: Atributo specularity de VML
ms.assetid: df04c15c-cfad-4172-81fa-a28e13f205fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b44cc9e8d266ba5ca9c7acb960425d7d4b246145c2d29ba0cc23f668d4aa24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098945"
---
# <a name="vml-specularity-attribute"></a>Atributo specularity de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la especulación de una forma extruida. Lectura/escritura **Numbernumber .**

**Se aplica a**

[Extrusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: *element* specularity=" *expression* ">

**Sintaxis de script**

*element* .specularity="*expression*"

*expresión* = *element*.specularity

**Comentarios:**

Este valor define la proporción de la luz del incidente con la luz reflejada especularmente. Los valores normales van de 0 a 1. El valor predeterminado es 0.

Si se especifican valores mayores que 1, pueden producirse efectos inusuales.

Microsoft Office Atributo Extensions

 

 