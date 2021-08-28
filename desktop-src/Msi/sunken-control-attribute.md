---
description: Si se establece este bit, el control se muestra con un aspecto tridimensional y desconsolado.
ms.assetid: 00052b01-f2f0-4749-8826-084e5ebb300a
title: Atributo de control bloqueado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3547f06d82a66a08a575958eac728051c3315f3382529065c3792cfdb94def
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626935"
---
# <a name="sunken-control-attribute"></a>Atributo de control bloqueado

Si se establece este bit, el control se muestra con un aspecto tridimensional y desconsolado. El efecto de este bit de estilo es diferente en los distintos controles y versiones de Windows. En algunos controles no tiene ningún efecto visible. Si el sistema no admite el atributo de control Sunken, el control se muestra en el estilo visual predeterminado. Si no se establece este bit, el control se muestra con el estilo visual predeterminado.

## <a name="valid-controls"></a>Controles válidos

Todos los controles.

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                         |
|---------|-------------|----------------------------------|
| 4       | 0x00000004  | **msidbControlAttributesSunken** |



 

## <a name="remarks"></a>Comentarios

Para establecer este atributo en un control, incluya el bit Sunken en la columna Attributes del registro del control en la [tabla Control](control-table.md).

Vea [Controles y atributos](control-attributes.md) de [control.](controls.md)

 

 



