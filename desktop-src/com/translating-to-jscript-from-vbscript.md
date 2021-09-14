---
title: Traducción a JScript desde VBScript
description: Traducción a JScript desde VBScript
ms.assetid: cdf04a01-8bc3-4f37-872b-3a0aae962f26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18c2ccb11ffa4f5f000d8cfc73f7db6f857cf6b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253034"
---
# <a name="translating-to-jscript-from-vbscript"></a>Traducción a JScript desde VBScript

En VBScript, **for**... **Cada** bucle enumera los miembros de una colección; en JScript, **para**... **en** bucle enumera los miembros de una JScript objeto o matriz. Para enumerar una colección en JScript, use un objeto Enumerator.

En JScript, hay varios tipos de datos, como números, cadenas, booleanos, objetos y el atributo NULL. VBScript solo usa un tipo de datos, **Variant**, que se puede subtipor para representar cadenas, números, booleanos, y así sucesivamente.

En JScript, las matrices se pueden expandir dinámicamente estableciendo un nuevo valor para la propiedad length de la matriz. En VBScript, las matrices no se pueden ampliar; se deben volver adimensionar mediante la **instrucción redim.**

VbScript y JScript admiten funciones. Sin embargo, VBScript también admite subrutinas. Las subrutinas son similares a las funciones, pero no devuelven un valor.

JScript distingue mayúsculas de minúsculas. VBScript no lo es.

JScript es compatible con Internet Explorer y Netscape Navigator. Netscape Navigator no admite VBScript.

JScript proporciona el objeto Error, que se puede usar para capturar y controlar errores. El objeto Error es análogo al objeto Err de VBScript.

JScript matrices no son matrices del tipo variable **VARIANT SAFEARRAY**. Si el script recibe una variable **VARIANT SAFEARRAY** de un objeto COM o un script VBScript, debe usar un objeto VBArray para tener acceso a la variable **VARIANT SAFEARRAY.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducción a JScript](translating-to-jscript.md)
</dt> </dl>

 

 




