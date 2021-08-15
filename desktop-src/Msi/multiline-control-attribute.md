---
description: Si este bit se establece en un control Editar, el instalador crea un control de edición de varias líneas con una barra de desplazamiento vertical.
ms.assetid: cbdbe088-9cf1-4af8-a5f7-072faee7f34e
title: Atributo de control multilínea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 474bf8a9b765f402924a554c9da064a8c60a01f6af910a3fd24c81d377978a93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943436"
---
# <a name="multiline-control-attribute"></a>Atributo de control multilínea

Si este bit se establece en un [control Editar](edit-control.md), el instalador crea un control de edición de varias líneas con una barra de desplazamiento vertical.

Si no se establece este bit, especifica que se muestra un control de edición normal.

## <a name="valid-controls"></a>Controles válidos

[Edite el control](edit-control.md).



| Decimal | Hexadecimal | Constante                            |
|---------|-------------|-------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesMultiline** |



 

## <a name="remarks"></a>Comentarios

Para establecer este atributo en un control , incluya el bit MultiLine en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Controles y atributos](control-attributes.md) de [control.](controls.md)

 

 



