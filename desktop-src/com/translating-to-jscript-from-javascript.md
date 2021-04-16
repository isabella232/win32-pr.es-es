---
title: Traducir a JScript desde JavaScript
description: Traducir a JScript desde JavaScript
ms.assetid: 86067a69-a6a1-474f-b8d8-85caf384a311
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45535807a5ef2baf59c2e068007a5a8df8bf4863
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104533027"
---
# <a name="translating-to-jscript-from-javascript"></a>Traducir a JScript desde JavaScript

JScript es compatible en gran medida con JavaScript. Sin embargo, JScript versión 5,0 incluye algunos objetos que no admite actualmente JavaScript, como ActiveXObject, Enumerator, error, global y VBArray.

JScript 5,0 admite el control de excepciones mediante **try**... instrucciones **catch** . JavaScript no proporciona actualmente un mecanismo de control de errores.

Al trabajar con JScript o JavaScript, existen algunas diferencias sutiles entre las implementaciones del modelo de objetos compatibles con varios exploradores Web. Para escribir un script que se ejecute en Internet Explorer y en Netscape Navigator, limite las características que usan los scripts a las que se especifican en el estándar de World Wide Web Consortium (W3C) para la versión 3,2 de HTML. Para obtener más información acerca de este estándar, consulte [especificación de referencia de HTML 3,2](https://www.w3.org/TR/REC-html32.html).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducir a JScript](translating-to-jscript.md)
</dt> </dl>

 

 




