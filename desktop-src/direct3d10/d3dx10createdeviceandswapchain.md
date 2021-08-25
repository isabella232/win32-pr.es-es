---
description: Cree el mejor dispositivo Direct3D y una cadena de intercambio.
ms.assetid: c320a6c4-fa68-47fc-b2cb-0dc53c2767e7
title: Función D3DX10CreateDeviceAndSwapChain (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDeviceAndSwapChain
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: aa92b0fd7efb9c6f457fd035fad28992d965a4cf2f6fdad39936292f7a70a996
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852375"
---
# <a name="d3dx10createdeviceandswapchain-function"></a>Función D3DX10CreateDeviceAndSwapChain

Cree el mejor dispositivo Direct3D y una cadena de intercambio.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10CreateDeviceAndSwapChain(
  _In_  IDXGIAdapter         *pAdapter,
  _In_  D3D10_DRIVER_TYPE    DriverType,
  _In_  HMODULE              Software,
  _In_  UINT                 Flags,
  _In_  DXGI_SWAP_CHAIN_DESC *pSwapChainDesc,
  _Out_ IDXGISwapChain       **ppSwapChain,
  _Out_ ID3D10Device         **ppDevice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAdapter* \[ En\]
</dt> <dd>

Tipo: **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***

Puntero a [**un IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).

</dd> <dt>

*DriverType* \[ En\]
</dt> <dd>

Tipo: **[ **TIPO DE \_ CONTROLADOR \_ D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**

Tipo de controlador para el dispositivo. Vea [**D3D10 \_ DRIVER \_ TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).

</dd> <dt>

*Software* \[ En\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Identificador del archivo DLL que implementa un rasterizador de software. Debe ser **NULL si** DriverType no es software. El HMODULE de un archivo DLL se puede obtener con [LoadLibrary,](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)o [GetModuleHandle.](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)

</dd> <dt>

*Marcas* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Opcional. Marcas de creación de dispositivos [**(consulte D3D10 \_ CREATE DEVICE \_ \_ FLAG)**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)que habilitan las [capas de API](d3d10-graphics-programming-guide-api-features-layers.md). Estas marcas pueden ser or bit a bit juntos.

</dd> <dt>

*pSwapChainDesc* \[ En\]
</dt> <dd>

Tipo: **[ **DXGI \_ SWAP \_ CHAIN \_ DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***

Descripción de la cadena de intercambio. Consulte [**DXGI \_ SWAP CHAIN \_ \_ DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc).

</dd> <dt>

*ppSwapChain* \[ out\]
</dt> <dd>

Tipo: **[ **IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***

Dirección de un puntero a [**un IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).

</dd> <dt>

*ppDevice* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Dirección de un puntero a una [**interfaz ID3D10Device que**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) recibirá el dispositivo recién creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Este método devuelve uno de los siguientes códigos de retorno [de Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Para crear el mejor dispositivo, este método implementa más de una opción de creación de dispositivos. En primer lugar, el método intenta crear un dispositivo 10.1 (y una cadena de intercambio). Si se produce un error, el método intenta crear un dispositivo 10.0. Si se produce un error, el método producirá un error. Si la aplicación solo necesita crear un dispositivo 10.1 o un dispositivo 10.0, use estas API en su lugar:

-   Use [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) para crear un dispositivo Direct3D 10.0 (solo) y una cadena de intercambio.
-   Use [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) para crear un dispositivo Direct3D 10.1 (solo) y una cadena de intercambio.

Este método requiere Windows Vista Service Pack 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Core.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[De uso general functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
