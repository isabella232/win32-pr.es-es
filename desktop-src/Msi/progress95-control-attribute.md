---
description: Si este bit se establece en un control ProgressBar, la barra se dibuja como una serie de rectángulos pequeños. Si no se establece este bit, la barra de indicador de progreso se dibuja como un rectángulo continuo único.
ms.assetid: b2c43763-799c-4f09-b9f8-47a4a5f4faf3
title: Atributo de control Progress95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2242dde671484274be946802ba4fd4c1cfd687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911657"
---
# <a name="progress95-control-attribute"></a>Atributo de control Progress95

Si este bit se establece en un [control ProgressBar](progressbar-control.md), la barra se dibuja como una serie de rectángulos pequeños. Si no se establece este bit, la barra de indicador de progreso se dibuja como un rectángulo continuo único.

## <a name="valid-controls"></a>Controles válidos

[ProgressBar](progressbar-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                             |
|---------|-------------|--------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesProgress95** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya el bit Progress95 en la columna Attributes del registro del control en la [tabla de control](control-table.md).

Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).

 

 



