---
title: Traducir a JScript desde VBScript
description: Traducir a JScript desde VBScript
ms.assetid: cdf04a01-8bc3-4f37-872b-3a0aae962f26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18c2ccb11ffa4f5f000d8cfc73f7db6f857cf6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773567"
---
# <a name="translating-to-jscript-from-vbscript"></a>Traducir a JScript desde VBScript

En VBScript, la **de**... **Cada** bucle enumera los miembros de una colección; en JScript, la **para**... **in** Loop enumera los miembros de un objeto o una matriz de JScript. Para enumerar una colección en JScript, use un objeto de enumerador.

En JScript, hay varios tipos de datos, como números, cadenas, valores booleanos, objetos y el atributo null. VBScript solo utiliza un tipo de datos, **Variant**, que se puede subescribir para representar cadenas, números, valores booleanos, etc.

En JScript, las matrices se pueden expandir dinámicamente estableciendo un nuevo valor para la propiedad Length de la matriz. En VBScript, no se pueden ampliar las matrices; se deben redimensionar con la instrucción **ReDim** .

Tanto VBScript como JScript admiten funciones. Sin embargo, VBScript también admite subrutinas. Las subrutinas son similares a las funciones, pero no devuelven un valor.

JScript distingue entre mayúsculas y minúsculas. VBScript no lo es.

JScript es compatible con Internet Explorer y Netscape Navigator. Netscape Navigator no es compatible con VBScript.

JScript proporciona el objeto de error, que se puede utilizar para interceptar y controlar los errores. El objeto error es análogo al objeto Err de VBScript.

Las matrices de JScript no son matrices del tipo de variable **Variant SafeArray**. Si el script recibe una variable **Variant de tipo SafeArray** de un objeto com o un script de VBScript, debe utilizar un objeto VBArray para tener acceso a la variable de **tipo SafeArray** de la variante.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducir a JScript](translating-to-jscript.md)
</dt> </dl>

 

 




