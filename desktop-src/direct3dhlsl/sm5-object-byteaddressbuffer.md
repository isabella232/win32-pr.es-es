---
title: ByteAddressBuffer
description: ByteAddressBuffer
ms.assetid: 809b5ee8-0a25-402e-8cf2-f5e7a8094ec6
keywords:
- HLSL de ByteAddressBuffer
topic_type:
- apiref
api_name:
- ByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03e89f56522d941db4447b33b55cbedc7c73303f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984074"
---
# <a name="byteaddressbuffer"></a>ByteAddressBuffer

Un búfer de solo lectura que se indiza en bytes.



| Método                                                              | Descripción                   |
|---------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-byteaddressbuffer-getdimensions.md) | Obtiene las dimensiones de recursos. |
| [**Carga**](byteaddressbuffer-load.md)                              | Obtiene un valor.               |
| [**Load2**](byteaddressbuffer-load2.md)                            | Obtiene dos valores.              |
| [**Load3**](byteaddressbuffer-load3.md)                            | Obtiene tres valores.            |
| [**Load4**](byteaddressbuffer-load4.md)                            | Obtiene cuatro valores.             |



 

Puede usar el tipo de objeto **ByteAddressBuffer** cuando trabaje con búferes sin procesar. Para obtener más información sobre la visualización sin formato de los búferes, consulte [vistas sin formato de búferes](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Este objeto es compatible con los siguientes modelos de sombreador.



| Modelo de sombreador                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Compatible |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| Sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador superiores modelo de sombreador [4](dx-graphics-hlsl-sm4.md) (disponible a través de la API de Direct3D 11 mediante el nivel de características 10,0 o 10,1 ([**\_ \_ nivel de característica D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) en los dispositivos que admiten los sombreadores de cálculo. Para obtener más información sobre la compatibilidad del sombreador de cálculo en el hardware de nivel inferior, vea [sombreadores de cálculo en hardware de nivel inferior](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders)).<br/> | sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

Para obtener más información sobre un búfer de direcciones de bytes, consulte el [tipo de recurso byte direccionable](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).

El modelo de sombreador 5 también implementa un [búfer de direcciones de bytes de lectura y escritura](sm5-object-rwbyteaddressbuffer.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

