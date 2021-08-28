---
description: El atributo de control indirecto especifica si se hace referencia indirectamente al valor mostrado o modificado por este control.
ms.assetid: dc9c0dd6-7e19-44ec-b1a5-3d51a1855adf
title: Atributo de control indirecto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c679938a818fb8393958c35694f3c2b7f782c91fc2dfcf1ac04777553ec629c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996695"
---
# <a name="indirect-control-attribute"></a>Atributo de control indirecto

El atributo de control indirecto especifica si se hace referencia indirectamente al valor mostrado o modificado por este control. Si se establece este bit, el control muestra o cambia el valor de la propiedad que tiene el identificador enumerado en la columna Propiedad de la [tabla Control](control-table.md). Si no se establece este bit, el control muestra o cambia el valor de la propiedad en la columna Propiedad de la tabla Control .

## <a name="valid-controls"></a>Controles válidos

Todos los controles activos.

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                           |
|---------|-------------|------------------------------------|
| 8       | 0x00000008  | **msidbControlAttributesIndirect** |



 

## <a name="remarks"></a>Comentarios

Vea [Atributos de](control-attributes.md) control y el control que debe crear en [Controles](controls.md).

 

 



