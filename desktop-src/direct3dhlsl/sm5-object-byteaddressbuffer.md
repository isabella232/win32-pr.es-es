---
title: ByteAddressBuffer
description: ByteAddressBuffer
ms.assetid: 809b5ee8-0a25-402e-8cf2-f5e7a8094ec6
keywords:
- ByteAddressBuffer HLSL
topic_type:
- apiref
api_name:
- ByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdb7a22570e92945df8ab599f8c95bdffa1d03dd9ac83e35dfc7bb849bd42d99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853335"
---
# <a name="byteaddressbuffer"></a>ByteAddressBuffer

Búfer de solo lectura que se indexa en bytes.



| Método                                                              | Descripción                   |
|---------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-byteaddressbuffer-getdimensions.md) | Obtiene las dimensiones de recursos. |
| [**Cargar**](byteaddressbuffer-load.md)                              | Obtiene un valor.               |
| [**Load2**](byteaddressbuffer-load2.md)                            | Obtiene dos valores.              |
| [**Load3**](byteaddressbuffer-load3.md)                            | Obtiene tres valores.            |
| [**Load4**](byteaddressbuffer-load4.md)                            | Obtiene cuatro valores.             |



 

Puede usar el tipo **de objeto ByteAddressBuffer** cuando trabaje con búferes sin procesar. Para obtener más información sobre la visualización sin procesar de búferes, vea [Raw Views of Buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este objeto se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Compatible |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| Modelo de sombreador [5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores Shader [Model 4](dx-graphics-hlsl-sm4.md) (disponible a través de la API de Direct3D 11 mediante el nivel de característica 10.0 o 10.1 ([**D3D \_ FEATURE \_ LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)10 X) en dispositivos que admiten sombreadores \_ \_ de proceso. Para obtener más información sobre la compatibilidad del sombreador de proceso en hardware de nivel inferior, vea [Sombreadores de proceso en hardware de nivel inferior).](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders)<br/> | Sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

Para obtener más información sobre un búfer de direcciones de bytes, vea el tipo de recurso [direccionable de bytes](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).

El modelo de sombreador 5 también implementa un búfer [de direcciones de bytes de lectura y escritura.](sm5-object-rwbyteaddressbuffer.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

