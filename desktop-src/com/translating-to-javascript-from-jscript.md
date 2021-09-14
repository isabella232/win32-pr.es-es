---
title: Traducción a JavaScript desde JScript
description: Traducción a JavaScript desde JScript
ms.assetid: 11d31c8c-868d-4220-9298-6d24a209dc47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b18972f407cf008626245798b3f7740d98058e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253059"
---
# <a name="translating-to-javascript-from-jscript"></a>Traducción a JavaScript desde JScript

JScript es compatible en gran medida con JavaScript. Sin embargo, JScript incluye algunos objetos no compatibles actualmente con JavaScript, como ActiveXObject, Enumerator, Error, Global y VBArray.

JScript versión 5.0 admite el control de excepciones mediante **try**... **instrucciones catch.** JavaScript no proporciona actualmente un mecanismo de entrega de errores.

Al trabajar con JScript o JavaScript, hay algunas diferencias sutiles entre las implementaciones del modelo de objetos compatibles con varios exploradores web. Para escribir un script que se ejecute en Internet Explorer y Netscape Navigator, limite las características que usan los scripts a las especificadas en el estándar World Wide Web Consortium (W3C) para HTML versión [3.2.](https://www.w3.org/tr/rec-html32.html)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducción a JavaScript](translating-to-javascript.md)
</dt> </dl>

 

 




