---
title: Traducir a VBScript desde JavaScript
description: Traducir a VBScript desde JavaScript
ms.assetid: f302e032-4e94-42f1-839b-022dab538760
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eda8169a665dc93133f7ac933de12ecc612f3e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714145"
---
# <a name="translating-to-vbscript-from-javascript"></a>Traducir a VBScript desde JavaScript

En JavaScript, hay varios tipos de datos, como números, cadenas, valores booleanos, objetos y el atributo null. VBScript solo utiliza un tipo de datos, **Variant**, que se puede subescribir para representar cadenas, números, valores booleanos, etc.

En JavaScript, las matrices se pueden expandir dinámicamente estableciendo un nuevo valor para la propiedad Length de la matriz. En VBScript, no se pueden ampliar las matrices; se deben redimensionar con la instrucción **ReDim** .

Tanto VBScript como JavaScript admiten funciones. Sin embargo, VBScript también admite subrutinas. Las subrutinas son similares a las funciones, salvo que no devuelven un valor.

JavaScript distingue mayúsculas de minúsculas. VBScript no lo es.

JavaScript es compatible con una amplia variedad de exploradores Web, incluidos Internet Explorer y Netscape Navigator. Netscape Navigator no es compatible con VBScript.

VBScript admite el control de errores a través de su objeto Err. JavaScript no proporciona actualmente un medio para interceptar y controlar errores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducir a VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




