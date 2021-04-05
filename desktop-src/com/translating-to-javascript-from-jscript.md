---
title: Traducir a JavaScript desde JScript
description: Traducir a JavaScript desde JScript
ms.assetid: 11d31c8c-868d-4220-9298-6d24a209dc47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b18972f407cf008626245798b3f7740d98058e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420367"
---
# <a name="translating-to-javascript-from-jscript"></a>Traducir a JavaScript desde JScript

JScript es compatible en gran medida con JavaScript. Sin embargo, JScript incluye algunos objetos que no son compatibles actualmente con JavaScript, como ActiveXObject, Enumerator, error, global y VBArray.

La versión 5,0 de JScript admite el control de excepciones mediante **try**... instrucciones **catch** . JavaScript no proporciona actualmente un mecanismo de control de errores.

Al trabajar con JScript o JavaScript, existen algunas diferencias sutiles entre las implementaciones del modelo de objetos compatibles con varios exploradores Web. Para escribir un script que se ejecute en Internet Explorer y en Netscape Navigator, limite las características que usan los scripts a las que se especifican en el estándar de World Wide Web Consortium (W3C) [para la versión 3,2 de HTML](https://www.w3.org/tr/rec-html32.html).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducir a JavaScript](translating-to-javascript.md)
</dt> </dl>

 

 




