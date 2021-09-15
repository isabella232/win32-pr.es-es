---
title: RWByteAddressBuffer
description: Búfer de lectura y escritura que indexa en bytes.
ms.assetid: 8370c14c-5822-4240-942d-565aa223d48c
keywords:
- RWByteAddressBuffer HLSL
topic_type:
- apiref
api_name:
- RWByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d065926b0769e15284cbe705783be012d82554b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466049"
---
# <a name="rwbyteaddressbuffer"></a>RWByteAddressBuffer

Búfer de lectura y escritura que indexa en bytes.



| Método                                                                                          | Descripción                         |
|-------------------------------------------------------------------------------------------------|-------------------------------------|
| [**GetDimensions**](sm5-object-rwbyteaddressbuffer-getdimensions.md)                           | Obtiene las dimensiones de recursos.       |
| [**InterlockedAdd**](sm5-object-rwbyteaddressbuffer-interlockedadd.md)                         | Agrega, de forma atómica.                   |
| [**InterlockedAnd**](sm5-object-rwbyteaddressbuffer-interlockedand.md)                         | AND, de forma atómica.                   |
| [**InterlockedCompareExchange**](sm5-object-rwbyteaddressbuffer-interlockedcompareexchange.md) | Compara e intercambia, de forma atómica. |
| [**InterlockedCompareStore**](sm5-object-rwbyteaddressbuffer-interlockedcomparestore.md)       | Compara y almacena de forma atómica.    |
| [**InterlockedExchange**](sm5-object-rwbyteaddressbuffer-interlockedexchange.md)               | Intercambios, de forma atómica.              |
| [**InterlockedMax**](sm5-object-rwbyteaddressbuffer-interlockedmax.md)                         | Busca el valor máximo de forma atómica.          |
| [**InterlockedMin**](sm5-object-rwbyteaddressbuffer-interlockedmin.md)                         | Busque el valor mínimo, de forma atómica.           |
| [**InterlockedOr**](sm5-object-rwbyteaddressbuffer-interlockedor.md)                           | Unidades de operación, de forma atómica.                    |
| [**InterlockedXor**](sm5-object-rwbyteaddressbuffer-interlockedxor.md)                         | XR, de forma atómica.                   |
| [**Carga**](rwbyteaddressbuffer-load.md)                                                        | Obtiene un valor.                     |
| [**Load2**](rwbyteaddressbuffer-load2.md)                                                      | Obtiene dos valores.                    |
| [**Load3**](rwbyteaddressbuffer-load3.md)                                                      | Obtiene tres valores.                  |
| [**Load4**](rwbyteaddressbuffer-load4.md)                                                      | Obtiene cuatro valores.                   |
| [**Tienda**](sm5-object-rwbyteaddressbuffer-store.md)                                           | Establece un valor.                     |
| [**Store2**](sm5-object-rwbyteaddressbuffer-store2.md)                                         | Establece dos valores.                    |
| [**Store3**](sm5-object-rwbyteaddressbuffer-store3.md)                                         | Establece tres valores.                  |
| [**Store4**](sm5-object-rwbyteaddressbuffer-store4.md)                                         | Establece cuatro valores.                   |



 

Los objetos RWByteAddressBuffer pueden tener como prefijo la clase de almacenamiento **globalmentecoherente**. Esta clase de almacenamiento hace que las barreras de memoria y las sincronizaciones vaciarán los datos en toda la GPU para que otros grupos puedan ver escrituras. Sin este especificador, una barrera o sincronización de memoria vaciará un UAV solo dentro del grupo actual.

El formato UAV enlazado a este recurso debe crearse con el formato DXGI \_ FORMAT \_ R32 \_ TYPELESS.

El UAV enlazado a este recurso debe haber sido creado con [**D3D11 \_ BUFFER \_ UAV \_ FLAG \_ RAW.**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag)

Puede usar el tipo **de objeto RWByteAddressBuffer** cuando trabaje con búferes sin procesar. Para obtener más información sobre la visualización sin formato de los búferes, vea [Raw Views of Buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este objeto se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Compatible |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| Modelo de sombreador [5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores Shader [Model 4](dx-graphics-hlsl-sm4.md) (disponible a través de la API de Direct3D 11 mediante el nivel de característica 10.0 o 10.1 [**(D3D \_ FEATURE \_ LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 X) en dispositivos que admiten sombreadores \_ de proceso. Para obtener más información sobre la compatibilidad del sombreador de proceso en hardware de nivel inferior, vea [Sombreadores de proceso en hardware de nivel inferior).](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders)<br/> | sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

