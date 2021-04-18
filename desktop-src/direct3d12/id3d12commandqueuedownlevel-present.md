---
title: ID3D12CommandQueueDownlevel::P método reenviado
description: Copia el contenido de un recurso de Texture2D de Direct3D 12 en una ventana. | ID3D12CommandQueueDownlevel::P método reenviado
keywords:
- Método Present
- Método Present, interfaz ID3D12CommandQueueDownlevel
- Interfaz ID3D12CommandQueueDownlevel, método present
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
ms.openlocfilehash: a6c74685911e52a671eaeb02645754a45b8d647e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721488"
---
# <a name="id3d12commandqueuedownlevelpresent-method"></a>ID3D12CommandQueueDownlevel::P método reenviado

Copia el contenido de un recurso de Texture2D de Direct3D 12 en una ventana.

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

Una lista de comandos abierta, que Direct3D 12 pone en cola un comando presente y, a continuación, se cierra y se envía automáticamente.

`pSourceTex2D`

Tipo: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***

Un recurso que contiene el contenido deseado que se va a mostrar, con la [**dimensión de recursos Dimension D3D12 \_ \_ \_ TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension), y un formato que es uno de los siguientes.

* DXGI_FORMAT_R16G16B16A16_FLOAT
* DXGI_FORMAT_R10G10B10A2_UNORM
* DXGI_FORMAT_R8G8B8A8_UNORM
* DXGI_FORMAT_R8G8B8A8_UNORM_SRGB
* DXGI_FORMAT_B8G8R8X8_UNORM
* DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM
* DXGI_FORMAT_B8G8R8A8_UNORM
* DXGI_FORMAT_B8G8R8A8_UNORM_SRGB

`hWindow`

Tipo: **[hWnd](/windows/desktop/WinProg/windows-data-types)**

Identificador de la ventana en la que se debe mostrar el contenido.

`Flags`

Tipo: **[D3D12 \_ de \_ presentación \_ de nivel inferior](d3d12_downlevel_present_flags.md)**

Marcas para modificar la operación **actual** .

## <a name="return-value"></a>Valor devuelto

Devuelve **S_OK** si se ejecuta correctamente o, de lo contrario, un HRESULT con error.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------|------------------|
| Encabezado | d3d12downlevel. h |
| Archivo DLL    | D3D12.dll (solo Windows 7) |

## <a name="see-also"></a>Vea también
* [ID3D12CommandQueueDownlevel](id3d12commandqueuedownlevel.md)
* [Direct3D 12 en interfaces de Windows 7](direct3d-12on7-interfaces.md)
* [Referencia de Direct3D 12 en Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 en Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
