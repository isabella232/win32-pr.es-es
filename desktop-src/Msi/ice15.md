---
description: ICE15 valida que el tipo de contenido y las referencias de extensión de MIME y las tablas de extensión sean recíprocos. La tabla MIME debe hacer referencia a un tipo de contenido a una extensión a la que la tabla de extensión hace referencia al mismo tipo de contenido.
ms.assetid: 8a38c8d2-324d-4de9-932b-d188ff5ccbaf
title: ICE15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb39b3c617db41e9e58a226f1eeb92c3d733ebad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082929"
---
# <a name="ice15"></a>ICE15

ICE15 valida que el tipo de contenido y las referencias de extensión de [MIME](mime-table.md) y las tablas de [extensión](extension-table.md) sean recíprocos. La tabla MIME debe hacer referencia a un tipo de contenido a una extensión a la que la tabla de extensión hace referencia al mismo tipo de contenido.

Varias extensiones pueden hacer referencia al mismo tipo MIME, siempre que el tipo MIME haga referencia a una de las extensiones. Varios tipos MIME pueden hacer referencia a la misma extensión, siempre y cuando la extensión haga referencia de nuevo a uno de los tipos MIME.

Tenga en cuenta que cada vez que un MIME hace referencia a una extensión, esa extensión no puede tener la \_ columna MIME en la tabla de extensión establecida en NULL.

## <a name="result"></a>Resultado

ICE15 publica un error si el tipo de contenido y las referencias de extensión no son recíprocos.

## <a name="example"></a>Ejemplo

ICE15 envía dos mensajes de error para el ejemplo mostrado:

-   El tipo de contenido test/solapas de la tabla MIME hace referencia a la extensión TST, pero la extensión TST en la tabla de la extensión hace referencia a las aletas/x-solapas. Esto no es recíproco.
-   Las solapas de tipo de contenido/solapas hacen referencia a la extensión FLP, pero esa extensión tiene una entrada nula en la \_ columna MIME de la tabla de extensión.

[Tabla MIME](mime-table.md) (parcial)



| ContentType   | Extensión\_ |
|---------------|-------------|
| prueba/x-prueba   | TST         |
| solapas/solapas | FLP         |



 

[Tabla de extensión](extension-table.md) (parcial)



| Extensión | Mine\_        |
|-----------|---------------|
| TST       | solapas/solapas |
| FLP       | Null          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



