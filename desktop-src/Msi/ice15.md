---
description: ICE15 valida que las referencias de tipo de contenido y extensión de las tablas MIME y Extension sean recíprocos. La tabla MIME debe hacer referencia a un tipo de contenido a una extensión a la que la tabla De extensión hace referencia al mismo tipo de contenido.
ms.assetid: 8a38c8d2-324d-4de9-932b-d188ff5ccbaf
title: ICE15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce1e5e54dedd2663a9f849abee43e244c73d7aa5835426be05d4e0163f599ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529315"
---
# <a name="ice15"></a>ICE15

ICE15 valida que las referencias de tipo de contenido y extensión de las [tablas MIME](mime-table.md) [y Extension](extension-table.md) sean recíprocos. La tabla MIME debe hacer referencia a un tipo de contenido a una extensión a la que la tabla De extensión hace referencia al mismo tipo de contenido.

Varias extensiones pueden hacer referencia al mismo tipo MIME, siempre y cuando el tipo MIME vuelva a hacer referencia a una de las extensiones. Varios tipos MIME pueden hacer referencia a la misma extensión, siempre y cuando la extensión vuelva a hacer referencia a uno de los tipos MIME.

Tenga en cuenta que siempre que un MIME hace referencia a una extensión, esa extensión no puede tener la columna MIME \_ de la tabla Extension establecida en Null.

## <a name="result"></a>Resultado

ICE15 publica un error si las referencias de tipo de contenido y extensión no son recíprocos.

## <a name="example"></a>Ejemplo

ICE15 publica dos mensajes de error para el ejemplo mostrado:

-   El tipo de contenido test/x-flaps de la tabla MIME hace referencia a la extensión tst, pero el tst de extensión de la tabla De extensión hace referencia a las referencias de las pilas/x-contras. Esto no es recíproco.
-   El tipo de contenido que hace referencia a la extensión flp, pero esa extensión tiene una entrada NULL en la columna MIME \_ de la tabla Extension.

[Tabla MIME](mime-table.md) (parcial)



| ContentType   | Extensión\_ |
|---------------|-------------|
| test/x-test   | Tst         |
| y/x-to-to-x | Flp         |



 

[Tabla de extensiones](extension-table.md) (parcial)



| Extensión | Mime\_        |
|-----------|---------------|
| Tst       | y/x-to-to-x |
| Flp       | Null          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



