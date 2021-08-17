---
title: Traducción a JScript desde JavaScript
description: Traducción a JScript desde JavaScript
ms.assetid: 86067a69-a6a1-474f-b8d8-85caf384a311
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c25276d569c5b461693a666d1bf8cf706b6896c0995972e1d2af0071c5760b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129567"
---
# <a name="translating-to-jscript-from-javascript"></a>Traducción a JScript desde JavaScript

JScript es compatible en gran medida con JavaScript. Sin embargo, JScript versión 5.0 incluye algunos objetos no compatibles actualmente con JavaScript, como ActiveXObject, Enumerator, Error, Global y VBArray.

JScript 5.0 admite el control de excepciones a través **de try**... **instrucciones catch.** JavaScript no proporciona actualmente un mecanismo de entrega de errores.

Al trabajar con JScript o JavaScript, hay algunas diferencias sutiles entre las implementaciones del modelo de objetos admitidas por varios exploradores web. Para escribir un script que se ejecute en Internet Explorer y Netscape Navigator, limite las características que usan los scripts a las especificadas en el estándar World Wide Web Consortium (W3C) para HTML versión 3.2. Para obtener más información sobre este estándar, vea [Especificación de referencia de HTML 3.2.](https://www.w3.org/TR/REC-html32.html)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducción a JScript](translating-to-jscript.md)
</dt> </dl>

 

 




