---
title: Traducción a VBScript desde JScript
description: Traducción a VBScript desde JScript
ms.assetid: db1115e1-2abd-4b06-ad8d-c1f917cd3087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3900ba82b258e6ee19cf06edb2f97247033778da5fcabaffe4a854e66a5fef73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992255"
---
# <a name="translating-to-vbscript-from-jscript"></a>Traducción a VBScript desde JScript

En VBScript, **for**... **Cada** bucle enumera los miembros de una colección; en JScript, **para**... **En** el bucle in se enumeran los miembros de una JScript o una matriz. Para enumerar una colección en JScript, use un objeto Enumerador.

JScript proporciona el objeto Error, que se puede usar para capturar y controlar los errores. El objeto Error es análogo al objeto Err de VBScript.

En JScript, hay varios tipos de datos, como números, cadenas, booleanos, objetos y el atributo NULL. VBScript solo usa un tipo de datos, **Variant**, que se puede subtipor para representar cadenas, números, booleanos, y así sucesivamente.

En JScript, las matrices se pueden expandir dinámicamente estableciendo un nuevo valor para la propiedad length de la matriz. En VBScript, las matrices no se pueden ampliar; se deben volver adimensionar mediante la **instrucción redim.**

VbScript y JScript admiten funciones. Sin embargo, VBScript también admite subrutinas. Las subrutinas son similares a las funciones, pero no devuelven un valor.

JScript distingue mayúsculas de minúsculas. VBScript no lo es.

JScript es compatible con una amplia variedad de exploradores web, incluidos Internet Explorer y Netscape Navigator. Netscape Navigator no admite VBScript.

JScript matrices no son matrices del tipo variable **VARIANT SAFEARRAY**. Un JScript script debe usar un objeto VBArray para tener acceso a la variable **VARIANT SAFEARRAY.** Los scripts de VBScript pueden acceder directamente a las variables **VARIANT SAFEARRAY.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducción a VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




