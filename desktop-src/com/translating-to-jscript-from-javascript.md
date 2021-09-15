---
title: Traducción a JScript desde JavaScript
description: Traducción a JScript desde JavaScript
ms.assetid: 86067a69-a6a1-474f-b8d8-85caf384a311
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45535807a5ef2baf59c2e068007a5a8df8bf4863
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571893"
---
# <a name="translating-to-jscript-from-javascript"></a>Traducción a JScript desde JavaScript

JScript es compatible en gran medida con JavaScript. Sin embargo, JScript versión 5.0 incluye algunos objetos no compatibles actualmente con JavaScript, como ActiveXObject, Enumerator, Error, Global y VBArray.

JScript 5.0 admite el control de excepciones mediante **try**... **instrucciones catch.** JavaScript no proporciona actualmente un mecanismo de entrega de errores.

Al trabajar con JScript o JavaScript, hay algunas diferencias sutiles entre las implementaciones del modelo de objetos compatibles con varios exploradores web. Para escribir un script que se ejecute en Internet Explorer y Netscape Navigator, limite las características usadas por los scripts a las especificadas en el estándar World Wide Web Consortium (W3C) para la versión 3.2 de HTML. Para obtener más información sobre este estándar, vea Especificación de [referencia de HTML 3.2.](https://www.w3.org/TR/REC-html32.html)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducción a JScript](translating-to-jscript.md)
</dt> </dl>

 

 




