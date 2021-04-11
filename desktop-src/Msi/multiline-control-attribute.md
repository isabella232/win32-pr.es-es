---
description: Si este bit se establece en un control de edición, el instalador crea un control de edición de varias líneas con una barra de desplazamiento vertical.
ms.assetid: cbdbe088-9cf1-4af8-a5f7-072faee7f34e
title: Atributo de control Multiline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936bc4b3901293e950690e878a0f86229bb03b4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276283"
---
# <a name="multiline-control-attribute"></a>Atributo de control Multiline

Si este bit se establece en un [control de edición](edit-control.md), el instalador crea un control de edición de varias líneas con una barra de desplazamiento vertical.

Si no se establece este bit, especifica que se muestra un control de edición normal.

## <a name="valid-controls"></a>Controles válidos

[Control de edición](edit-control.md).



| Decimal | Hexadecimal | Constante                            |
|---------|-------------|-------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesMultiline** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya el bit de varias líneas en la columna Attributes del registro del control en la [tabla de control](control-table.md).

Vea [controles y](controls.md) [atributos de control](control-attributes.md) .

 

 



