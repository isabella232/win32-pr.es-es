---
description: Constantes utilizadas para establecer la prioridad de un recurso en SetPriority.
ms.assetid: 98886349-883f-41c3-870b-e4a639977760
title: D3D9_RESOURCE_PRIORITY (D3d9types. h)
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
ms.openlocfilehash: 1ae5a54c7645db63b1023c3571f8181f4ee2daec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280271"
---
# <a name="d3d9_resource_priority"></a>Prioridad de los recursos de D3D9 \_ \_

Constantes utilizadas para establecer la prioridad de un recurso en [**SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority).



| Constante o valor                                                                                                                                                                                                                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3D9_RESOURCE_PRIORITY_MINIMUM"></span><span id="d3d9_resource_priority_minimum"></span><dl> <dt>**D3D9 \_ 0x28000000 \_ \_ mínima de prioridad de recursos**</dt> <dt></dt> </dl> | El recurso tiene la prioridad más baja posible. Esta constante marca el recurso como no utilizado y para la expulsión. El recurso debe expulsarse en cuanto otro recurso requiera el espacio de memoria que ocupa el recurso.<br/>                                                                                                                                                                                                              |
| <span id="D3D9_RESOURCE_PRIORITY_LOW"></span><span id="d3d9_resource_priority_low"></span><dl> <dt>**D3D9 \_ Prioridad de recursos \_ \_ bajo**</dt> <dt>0x50000000</dt> </dl>             | El recurso está programado con prioridad baja. La colocación del recurso no es crítica y el sistema operativo realiza un trabajo mínimo para encontrar una ubicación para el recurso. Marcar un recurso como de prioridad baja permite que otros recursos más críticos ocupen la memoria más rápida.<br/>                                                                                                                                                      |
| <span id="D3D9_RESOURCE_PRIORITY_NORMAL"></span><span id="d3d9_resource_priority_normal"></span><dl> <dt>**D3D9 \_ 0x78000000 \_ \_ normal de prioridad de recursos**</dt> <dt></dt> </dl>    | El recurso se programa con prioridad normal. La colocación del recurso es importante para el rendimiento, pero no es fundamental. El sistema operativo debe intentar colocar el recurso que está marcado como normal en la ubicación preferida del recurso en lugar de un recurso de prioridad baja. Normalmente, las texturas se marcan como normales.<br/>                                                                                                     |
| <span id="D3D9_RESOURCE_PRIORITY_HIGH"></span><span id="d3d9_resource_priority_high"></span><dl> <dt>**D3D9 \_ Prioridad de recursos \_ \_ alta**</dt> <dt>0xa0000000</dt> </dl>          | El recurso está programado con prioridad alta. La colocación del recurso es fundamental para el rendimiento. El sistema operativo siempre intenta colocar el recurso marcado como alto en la ubicación preferida del recurso en lugar de un recurso de prioridad baja o normal. Normalmente, los destinos de representación se marcan como alto.<br/>                                                                                                         |
| <span id="D3D9_RESOURCE_PRIORITY_MAXIMUM"></span><span id="d3d9_resource_priority_maximum"></span><dl> <dt>**D3D9 \_ \_ \_ Número máximo de prioridades de recursos**</dt> <dt>0xc8000000</dt> </dl> | El recurso tiene la máxima prioridad posible. Esta constante marca la prioridad del recurso como anclado flexible. Un recurso anclado provisional se expulsa de la memoria solo si no hay otra manera de resolver los requisitos de memoria de un búfer DMA. El sistema operativo intenta dividir un búfer DMA a su tamaño mínimo y expulsar todos los demás recursos que no están anclados y no se anclan de software antes de expulsar un recurso anclado de software. <br/> |



## <a name="remarks"></a>Observaciones

El programador trata los valores distintos de la **\_ prioridad del recurso D3D9 \_ \_ Minimum** y **D3D9 \_ \_ \_ Maximum Priority** como sugerencias.

Puede usar niveles de prioridad distintos de los definidos anteriormente en este tema. Por ejemplo, al marcar un recurso con un nivel de prioridad de 0x78000001, se indica que la prioridad del recurso está ligeramente por encima de lo normal.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
