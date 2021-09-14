---
title: Método ID3D12DeviceDownlevel::QueryVideoMemoryInfo
description: Copia el contenido de un recurso de Texture2D de Direct3D 12 en una ventana. | Método ID3D12DeviceDownlevel::QueryVideoMemoryInfo
keywords:
- Método QueryVideoMemoryInfo
- Método QueryVideoMemoryInfo, interfaz ID3D12DeviceDownlevel
- Interfaz ID3D12DeviceDownlevel, método QueryVideoMemoryInfo
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel.QueryVideoMemoryInfo
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 32b93fcbbe44aaae0916e6d8f3f403eb960e26eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966827"
---
# <a name="id3d12devicedownlevelqueryvideomemoryinfo-method"></a>Método ID3D12DeviceDownlevel::QueryVideoMemoryInfo

Proporciona estadísticas de memoria en Windows 7. Este método es equivalente a [IDXGIAdapter3::QueryVideoMemoryInfo](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo), que no está disponible en Windows 7.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT QueryVideoMemoryInfo( 
    UINT NodeIndex,
    DXGI_MEMORY_SEGMENT_GROUP MemorySegmentGroup,
    DXGI_QUERY_VIDEO_MEMORY_INFO *pVideoMemoryInfo
);
```

## <a name="parameters"></a>Parámetros

`NodeIndex`

Tipo: **UINT**

Especifica el adaptador físico del dispositivo para el que se consulta la información de memoria de vídeo. Para la operación de GPU única, establezca esta opción en cero. Si hay varios nodos de GPU, establezca esta opción en el índice del nodo (el adaptador físico del dispositivo) para el que se consulta la información de memoria de vídeo. Consulte [Sistemas de varios adaptadores.](multi-engine.md)

`MemorySegmentGroup`

Tipo: **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**

Especifica un **DXGI_MEMORY_SEGMENT_GROUP** que identifica el grupo como local o no local.

`pVideoMemoryInfo`

Tipo: **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***

Rellena una estructura **DXGI_QUERY_VIDEO_MEMORY_INFO** con los valores actuales.

## <a name="return-value"></a>Valor devuelto

Devuelve **S_OK** correcto o, de lo contrario, un HRESULT con error.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------|------------------|
| Encabezado | d3d12downlevel.h y dxgi1_4.h |
| Archivo DLL    | D3D12.dll (solo Windows 7) |

## <a name="see-also"></a>Consulte también
* [ID3D12DeviceDownlevel](id3d12devicedownlevel.md)
* [Direct3D 12 en interfaces de Windows 7](direct3d-12on7-interfaces.md)
* [Direct3D 12 en Windows 7 (d3d12downlevel.h)](direct3d-12on7-reference.md)
* [Direct3D 12 en Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
