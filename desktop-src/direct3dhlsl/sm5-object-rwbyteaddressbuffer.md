---
title: RWByteAddressBuffer
description: Un búfer de lectura/escritura que indexa en bytes.
ms.assetid: 8370c14c-5822-4240-942d-565aa223d48c
keywords:
- HLSL de RWByteAddressBuffer
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
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420742"
---
# <a name="rwbyteaddressbuffer"></a>RWByteAddressBuffer

Un búfer de lectura/escritura que indexa en bytes.



| Método                                                                                          | Descripción                         |
|-------------------------------------------------------------------------------------------------|-------------------------------------|
| [**GetDimensions**](sm5-object-rwbyteaddressbuffer-getdimensions.md)                           | Obtiene las dimensiones de recursos.       |
| [**InterlockedAdd**](sm5-object-rwbyteaddressbuffer-interlockedadd.md)                         | Agrega, de forma atómica.                   |
| [**InterlockedAnd**](sm5-object-rwbyteaddressbuffer-interlockedand.md)                         | And, de forma atómica.                   |
| [**InterlockedCompareExchange**](sm5-object-rwbyteaddressbuffer-interlockedcompareexchange.md) | Compara e intercambia, de forma atómica. |
| [**InterlockedCompareStore**](sm5-object-rwbyteaddressbuffer-interlockedcomparestore.md)       | Compara y almacena, de forma atómica.    |
| [**InterlockedExchange**](sm5-object-rwbyteaddressbuffer-interlockedexchange.md)               | Intercambios, de forma atómica.              |
| [**InterlockedMax**](sm5-object-rwbyteaddressbuffer-interlockedmax.md)                         | Busca el máximo, de forma atómica.          |
| [**InterlockedMin**](sm5-object-rwbyteaddressbuffer-interlockedmin.md)                         | Busque min, atomicly.           |
| [**Interbloqueo**](sm5-object-rwbyteaddressbuffer-interlockedor.md)                           | ORs, de forma atómica.                    |
| [**InterlockedXor**](sm5-object-rwbyteaddressbuffer-interlockedxor.md)                         | XORs, de forma atómica.                   |
| [**Carga**](rwbyteaddressbuffer-load.md)                                                        | Obtiene un valor.                     |
| [**Load2**](rwbyteaddressbuffer-load2.md)                                                      | Obtiene dos valores.                    |
| [**Load3**](rwbyteaddressbuffer-load3.md)                                                      | Obtiene tres valores.                  |
| [**Load4**](rwbyteaddressbuffer-load4.md)                                                      | Obtiene cuatro valores.                   |
| [**Store**](sm5-object-rwbyteaddressbuffer-store.md)                                           | Establece un valor.                     |
| [**2**](sm5-object-rwbyteaddressbuffer-store2.md)                                         | Establece dos valores.                    |
| [**Store3**](sm5-object-rwbyteaddressbuffer-store3.md)                                         | Establece tres valores.                  |
| [**Store4**](sm5-object-rwbyteaddressbuffer-store4.md)                                         | Establece cuatro valores.                   |



 

Los objetos RWByteAddressBuffer pueden ir precedidos de la clase de almacenamiento **globallycoherent**. Esta clase de almacenamiento provoca barreras de memoria y sincronizaciones para vaciar los datos en toda la GPU, de modo que otros grupos puedan ver escrituras. Sin este especificador, una barrera de memoria o una sincronización vaciará un UAV solo dentro del grupo actual.

El formato UAV enlazado a este recurso debe crearse con el formato DXGI sin \_ \_ \_ tipo R32.

El UAV enlazado a este recurso se debe haber creado con [**el \_ búfer de D3D11 UAV de \_ \_ marca \_ sin formato**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).

Puede usar el tipo de objeto **RWByteAddressBuffer** cuando trabaje con búferes sin procesar. Para obtener más información sobre la visualización sin formato de los búferes, consulte [vistas sin formato de búferes](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Este objeto es compatible con los siguientes modelos de sombreador.



| Modelo de sombreador                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Compatible |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| Sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador superiores modelo de sombreador [4](dx-graphics-hlsl-sm4.md) (disponible a través de la API de Direct3D 11 mediante el nivel de características 10,0 o 10,1 ([**\_ \_ nivel de característica D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) en los dispositivos que admiten los sombreadores de cálculo. Para obtener más información sobre la compatibilidad del sombreador de cálculo en el hardware de nivel inferior, vea [sombreadores de cálculo en hardware de nivel inferior](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).<br/> | sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

