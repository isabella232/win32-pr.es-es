---
description: El atributo de control indirecto especifica si se hace referencia indirectamente al valor mostrado o modificado por este control.
ms.assetid: dc9c0dd6-7e19-44ec-b1a5-3d51a1855adf
title: Atributo de control indirecto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d0c183f586c197b14810e7176bce607ac3adaf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171825"
---
# <a name="indirect-control-attribute"></a>Atributo de control indirecto

El atributo de control indirecto especifica si se hace referencia indirectamente al valor mostrado o modificado por este control. Si se establece este bit, el control muestra o cambia el valor de la propiedad que tiene el identificador enumerado en la columna Propiedad de la [tabla Control](control-table.md). Si no se establece este bit, el control muestra o cambia el valor de la propiedad en la columna Propiedad de la tabla Control .

## <a name="valid-controls"></a>Controles válidos

Todos los controles activos.

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                           |
|---------|-------------|------------------------------------|
| 8       | 0x00000008  | **msidbControlAttributesIndirect** |



 

## <a name="remarks"></a>Observaciones

Vea [Atributos de](control-attributes.md) control y el control que debe crear en [Controles](controls.md).

 

 



