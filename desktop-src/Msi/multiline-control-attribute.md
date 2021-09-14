---
description: Si este bit se establece en un control Editar, el instalador crea un control de edición de varias líneas con una barra de desplazamiento vertical.
ms.assetid: cbdbe088-9cf1-4af8-a5f7-072faee7f34e
title: Atributo de control multilínea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936bc4b3901293e950690e878a0f86229bb03b4d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071837"
---
# <a name="multiline-control-attribute"></a>Atributo de control multilínea

Si este bit se establece en un [control Editar](edit-control.md), el instalador crea un control de edición de varias líneas con una barra de desplazamiento vertical.

Si no se establece este bit, especifica que se muestra un control de edición normal.

## <a name="valid-controls"></a>Controles válidos

[Edite el control](edit-control.md).



| Decimal | Hexadecimal | Constante                            |
|---------|-------------|-------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesMultiline** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya el bit MultiLine en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Controles y atributos](control-attributes.md) de [control.](controls.md)

 

 



