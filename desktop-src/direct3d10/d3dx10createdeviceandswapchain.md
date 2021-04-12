---
description: Cree el mejor dispositivo Direct3D y una cadena de intercambio.
ms.assetid: c320a6c4-fa68-47fc-b2cb-0dc53c2767e7
title: Función D3DX10CreateDeviceAndSwapChain (D3DX10Core. h)
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
ms.openlocfilehash: fe71aeae91f8c43966e0fda2d2f430c7908f2855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362709"
---
# <a name="d3dx10createdeviceandswapchain-function"></a>D3DX10CreateDeviceAndSwapChain función)

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

*pAdapter* \[ de\]
</dt> <dd>

Tipo: **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***

Puntero a un [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).

</dd> <dt>

*DriverType* \[ de\]
</dt> <dd>

Tipo: **[ **\_ \_ tipo de controlador D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**

El tipo de controlador para el dispositivo. Consulte [**\_ \_ tipo de controlador D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).

</dd> <dt>

*Software* \[ de de\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Identificador del archivo DLL que implementa un rasterizador de software. Debe ser **null** si DriverType es no software. Los HMODULE de un archivo DLL se pueden obtener con [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)o [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Opcional. Marcas de creación de dispositivos (consulte [**D3D10 \_ Create \_ Device \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)) que habilitan las [capas de API](d3d10-graphics-programming-guide-api-features-layers.md). Estas marcas pueden ser OR bit a bit.

</dd> <dt>

*pSwapChainDesc* \[ de\]
</dt> <dd>

Tipo: **[ **\_ \_ \_ Descripción** de la cadena de intercambio de DXGI](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***

Descripción de la cadena de intercambio. Consulte [**la \_ \_ \_ Descripción**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)de la cadena de intercambio de DXGI.

</dd> <dt>

*ppSwapChain* \[ enuncia\]
</dt> <dd>

Tipo: **[ **IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***

Dirección de un puntero a un [**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).

</dd> <dt>

*ppDevice* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Dirección de un puntero a una [**interfaz ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) que recibirá el dispositivo recién creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Este método devuelve uno de los siguientes [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Para crear el mejor dispositivo, este método implementa más de una opción de creación de dispositivos. En primer lugar, el método intenta crear un dispositivo 10,1 (y una cadena de intercambio). Si se produce un error, el método intenta crear un dispositivo 10,0. Si se produce un error, se producirá un error en el método. Si su aplicación solo necesita crear un dispositivo 10,1 o un dispositivo 10,0, use estas API en su lugar:

-   Use [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) para crear un dispositivo Direct3D 10,0 (solo) y una cadena de intercambio.
-   Use [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) para crear un dispositivo Direct3D 10,1 (solo) y una cadena de intercambio.

Este método requiere Windows Vista Service Pack 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de De uso general](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
