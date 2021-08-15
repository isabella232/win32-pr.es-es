---
title: Id3D12CommandQueueDownlevel::P resent (método)
description: Copia el contenido de un recurso de Direct3D 12 Texture2D en una ventana. | Id3D12CommandQueueDownlevel::P resent (método)
keywords:
- Método Present
- Método present, interfaz ID3D12CommandQueueDownlevel
- Interfaz ID3D12CommandQueueDownlevel, método Present
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel.Present
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: b21a97d15d2666dcfe0a304f2393d6d14c5dbcc4142d8b42f43f295d8751614b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118529135"
---
# <a name="id3d12commandqueuedownlevelpresent-method"></a>Id3D12CommandQueueDownlevel::P resent (método)

Copia el contenido de un recurso de Direct3D 12 Texture2D en una ventana.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT Present
    ID3D12GraphicsCommandList *pOpenCommandList,
    ID3D12Resource *pSourceTex2D,
    HWND hWindow,
    D3D12_DOWNLEVEL_PRESENT_FLAGS Flags
);
```

## <a name="parameters"></a>Parámetros

`pOpenCommandList`

Tipo: **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

Una lista de comandos abierta, en la que Direct3D 12 coloca en cola un comando Present y, a continuación, se cierra y envía por usted.

`pSourceTex2D`

Tipo: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***

Recurso que contiene el contenido deseado que se va a mostrar, con la dimensión [**D3D12 \_ RESOURCE \_ DIMENSION \_ TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)y un formato que es uno de los siguientes.

* DXGI_FORMAT_R16G16B16A16_FLOAT
* DXGI_FORMAT_R10G10B10A2_UNORM
* DXGI_FORMAT_R8G8B8A8_UNORM
* DXGI_FORMAT_R8G8B8A8_UNORM_SRGB
* DXGI_FORMAT_B8G8R8X8_UNORM
* DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM
* DXGI_FORMAT_B8G8R8A8_UNORM
* DXGI_FORMAT_B8G8R8A8_UNORM_SRGB

`hWindow`

Tipo: **[HWND](/windows/desktop/WinProg/windows-data-types)**

Identificador de la ventana donde se debe mostrar el contenido.

`Flags`

Tipo: **[D3D12 \_ DOWNLEVEL \_ PRESENT \_ FLAGS](d3d12_downlevel_present_flags.md)**

Marcas para modificar la **operación** Present.

## <a name="return-value"></a>Valor devuelto

Devuelve **S_OK** correcto o, de lo contrario, un HRESULT con error.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------|------------------|
| Encabezado | d3d12downlevel.h |
| Archivo DLL    | D3D12.dll (solo Windows 7) |

## <a name="see-also"></a>Consulte también
* [ID3D12CommandQueueDownlevel](id3d12commandqueuedownlevel.md)
* [Direct3D 12 en interfaces de Windows 7](direct3d-12on7-interfaces.md)
* [Direct3D 12 en Windows referencia 7 (d3d12downlevel.h)](direct3d-12on7-reference.md)
* [Direct3D 12 en Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
