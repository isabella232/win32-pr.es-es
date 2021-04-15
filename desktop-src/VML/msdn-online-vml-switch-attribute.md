---
title: Atributo de modificador VML
description: Atributo de modificador VML
ms.assetid: fc099c0a-6789-41e8-ab08-36f4fd2d3bfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d102d6af20e698d8ec281cb1be6fae9690de4e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676386"
---
# <a name="vml-switch-attribute"></a>Atributo de modificador VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si las direcciones de identificador se intercambian. Lectura/escritura **VgTriState**.

**Se aplica a**

[H](msdn-online-vml-h-element.md) (subelemento de [Handles](msdn-online-vml-handles-element.md))

**Sintaxis de etiquetas**

<v: *Element* switch = " *expresión* " >

**Comentarios:**

Si es **true**, el identificador se cambia entre las direcciones x e y si la forma es más alta que ancha. El valor predeterminado es **False**.

Este atributo se usa para las formas con el comportamiento de stretch de limo.

*Atributo estándar de VML*

 

 