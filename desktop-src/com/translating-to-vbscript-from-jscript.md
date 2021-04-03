---
title: Traducir a VBScript desde JScript
description: Traducir a VBScript desde JScript
ms.assetid: db1115e1-2abd-4b06-ad8d-c1f917cd3087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f5ac608e94f883edc3b319fd04625e9a08d18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075412"
---
# <a name="translating-to-vbscript-from-jscript"></a>Traducir a VBScript desde JScript

En VBScript, la **de**... **Cada** bucle enumera los miembros de una colección; en JScript, la **para**... **in** Loop enumera los miembros de un objeto o una matriz de JScript. Para enumerar una colección en JScript, use un objeto de enumerador.

JScript proporciona el objeto de error, que se puede utilizar para interceptar y controlar los errores. El objeto error es análogo al objeto Err de VBScript.

En JScript, hay varios tipos de datos, como números, cadenas, valores booleanos, objetos y el atributo null. VBScript solo utiliza un tipo de datos, **Variant**, que se puede subescribir para representar cadenas, números, valores booleanos, etc.

En JScript, las matrices se pueden expandir dinámicamente estableciendo un nuevo valor para la propiedad Length de la matriz. En VBScript, no se pueden ampliar las matrices; se deben redimensionar con la instrucción **ReDim** .

Tanto VBScript como JScript admiten funciones. Sin embargo, VBScript también admite subrutinas. Las subrutinas son similares a las funciones, pero no devuelven un valor.

JScript distingue entre mayúsculas y minúsculas. VBScript no lo es.

JScript es compatible con una amplia variedad de exploradores Web, incluidos Internet Explorer y Netscape Navigator. Netscape Navigator no es compatible con VBScript.

Las matrices de JScript no son matrices del tipo de variable **Variant SafeArray**. Un script de JScript debe utilizar un objeto VBArray para tener acceso a la variable **Variant SafeArray**. Los scripts de VBScript pueden tener acceso directamente a las variables **SAFEARRAY de variante**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducir a VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




