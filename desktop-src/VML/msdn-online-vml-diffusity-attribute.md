---
title: Atributo Diffusity de VML
description: Atributo Diffusity de VML
ms.assetid: 1d131540-9166-47fc-bb0d-fada38f6a3de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b311c70e1cf49ece7f0072d70b07e886d11f0fe9122fc5d248a32f4321ba19b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754746"
---
# <a name="vml-diffusity-attribute"></a>Atributo Diffusity de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la cantidad de luz reflejada a partir de una forma extruida. Lectura/escritura **Numbernumber .**

**Se aplica a**

[Extrusión](msdn-online-vml-extrusion-element.md)

**Sintaxis de etiquetas**

<o: *element* diffusity=" *expression* ">

**Sintaxis de script**

*element* .diffusity="*expression*"

*expresión* = *elemento*.diffusity

**Comentarios:**

Este valor define la proporción entre la luz del incidente y la luz reflejada difusa. Los valores normales van de 0 a 1. El valor predeterminado es 0.

Si se especifican valores mayores que 1, pueden producirse efectos inusuales.

*Microsoft Office Atributo Extensions*

 

 