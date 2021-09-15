---
title: Traducción a VBScript desde JavaScript
description: Traducción a VBScript desde JavaScript
ms.assetid: f302e032-4e94-42f1-839b-022dab538760
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eda8169a665dc93133f7ac933de12ecc612f3e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568516"
---
# <a name="translating-to-vbscript-from-javascript"></a>Traducción a VBScript desde JavaScript

En JavaScript, hay varios tipos de datos, como números, cadenas, booleanos, objetos y el atributo NULL. VBScript solo usa un tipo de datos, **Variant**, que se puede subtipor para representar cadenas, números, booleanos, y así sucesivamente.

En JavaScript, las matrices se pueden expandir dinámicamente estableciendo un nuevo valor para la propiedad length de la matriz. En VBScript, las matrices no se pueden ampliar; se deben volver adimensionar mediante la **instrucción redim.**

VbScript y JavaScript admiten funciones. Sin embargo, VBScript también admite subrutinas. Las subrutinas son similares a las funciones, salvo que no devuelven un valor.

JavaScript distingue mayúsculas de minúsculas. VBScript no lo es.

JavaScript es compatible con una amplia variedad de exploradores web, incluidos Internet Explorer y Netscape Navigator. Netscape Navigator no admite VBScript.

VBScript admite el control de errores a través de su objeto Err. JavaScript no proporciona actualmente un medio de captura y control de errores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducción a VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




