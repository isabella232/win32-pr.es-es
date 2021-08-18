---
description: Constantes usadas para establecer la prioridad de un recurso en SetPriority.
ms.assetid: 98886349-883f-41c3-870b-e4a639977760
title: D3D9_RESOURCE_PRIORITY (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D9_RESOURCE_PRIORITY_MINIMUM
- D3D9_RESOURCE_PRIORITY_LOW
- D3D9_RESOURCE_PRIORITY_NORMAL
- D3D9_RESOURCE_PRIORITY_HIGH
- D3D9_RESOURCE_PRIORITY_MAXIMUM
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 367d50292b283cc7a0dcdef42b2e2c270099e314dc61c8d590e7ef2a1091a4f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751335"
---
# <a name="d3d9_resource_priority"></a>D3D9 \_ RESOURCE \_ PRIORITY

Constantes usadas para establecer la prioridad de un recurso en [**SetPriority.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority)



| Constante o valor                                                                                                                                                                                                                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3D9_RESOURCE_PRIORITY_MINIMUM"></span><span id="d3d9_resource_priority_minimum"></span><dl> <dt>**D3D9 \_ PRIORIDAD \_ MÍNIMA \_ DE**</dt> RECURSOS <dt>0x28000000</dt> </dl> | El recurso tiene la prioridad más baja posible. Esta constante marca el recurso como sin usar y para su expulsión. El recurso debe expulsarse en cuanto otro recurso requiera el espacio de memoria que ocupa el recurso.<br/>                                                                                                                                                                                                              |
| <span id="D3D9_RESOURCE_PRIORITY_LOW"></span><span id="d3d9_resource_priority_low"></span><dl> <dt>**D3D9 \_ PRIORIDAD \_ DE \_ RECURSOS BAJA**</dt> <dt>0x50000000</dt> </dl>             | El recurso se programa con prioridad baja. La colocación del recurso no es crítica y el sistema operativo realiza un trabajo mínimo para encontrar una ubicación para el recurso. Marcar un recurso como de prioridad baja permite que otros recursos más críticos ocupen la memoria más rápida.<br/>                                                                                                                                                      |
| <span id="D3D9_RESOURCE_PRIORITY_NORMAL"></span><span id="d3d9_resource_priority_normal"></span><dl> <dt>**D3D9 \_ Prioridad \_ de recursos \_ normal**</dt> <dt>0x78000000</dt> </dl>    | El recurso se programa con prioridad normal. La colocación del recurso es importante para el rendimiento, pero no es fundamental. El sistema operativo debe intentar colocar el recurso marcado como normal en la ubicación preferida del recurso en lugar de en un recurso de prioridad baja. Normalmente, las texturas se marcan como normales.<br/>                                                                                                     |
| <span id="D3D9_RESOURCE_PRIORITY_HIGH"></span><span id="d3d9_resource_priority_high"></span><dl> <dt>**D3D9 \_ PRIORIDAD \_ DE RECURSOS ALTA \_ 0xa0000000**</dt> <dt></dt> </dl>          | El recurso se programa con prioridad alta. La colocación del recurso es fundamental para el rendimiento. El sistema operativo siempre intenta colocar el recurso marcado como alto en la ubicación preferida del recurso en lugar de un recurso de prioridad baja o de prioridad normal. Normalmente, los destinos de representación se marcan como altos.<br/>                                                                                                         |
| <span id="D3D9_RESOURCE_PRIORITY_MAXIMUM"></span><span id="d3d9_resource_priority_maximum"></span><dl> <dt>**D3D9 \_ Prioridad \_ máxima \_ de**</dt> recursos <dt>0xc8000000</dt> </dl> | El recurso tiene la prioridad máxima posible. Esta constante marca la prioridad del recurso como anclado de forma flexible. Un recurso anclado de forma flexible se expulsa de la memoria solo si no hay otra manera de resolver el requisito de memoria de un búfer DMA. El sistema operativo intenta dividir un búfer de DMA en su tamaño mínimo y expulsar todos los demás recursos que no están anclados y no anclados de forma flexible antes de expulsar un recurso anclado de forma flexible. <br/> |



## <a name="remarks"></a>Comentarios

Los valores distintos de **D3D9 \_ RESOURCE \_ PRIORITY \_ MINIMUM** y **D3D9 \_ RESOURCE PRIORITY \_ \_ MAXIMUM** se tratan como sugerencias por parte del programador.

Puede usar niveles de prioridad distintos de los valores definidos anteriormente en este tema. Por ejemplo, marcar un recurso con un nivel de prioridad de 0x78000001 indica que la prioridad del recurso está ligeramente por encima de lo normal.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
