---
description: Cree el mejor dispositivo Direct3D 10 que representa el adaptador de pantalla. Si se puede crear un dispositivo compatible con Direct3D 10,1, será posible adquirir un puntero de interfaz ID3D10Device1 desde el puntero de interfaz de dispositivo devuelto.
ms.assetid: 1af8f4e5-a59e-403a-95d2-069b91bad93e
title: Función D3DX10CreateDevice (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDevice
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 38236a48cdd5197f7f19ef9be3f6fc0f1faca72c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718426"
---
# <a name="d3dx10createdevice-function"></a>D3DX10CreateDevice función)

Cree el mejor dispositivo Direct3D 10 que representa el adaptador de pantalla. Si se puede crear un dispositivo compatible con Direct3D 10,1, será posible adquirir un puntero de [**interfaz ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) desde el puntero de interfaz de dispositivo devuelto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10CreateDevice(
  _In_  IDXGIAdapter      *pAdapter,
  _In_  D3D10_DRIVER_TYPE DriverType,
  _In_  HMODULE           Software,
  _In_  UINT              Flags,
  _Out_ ID3D10Device      **ppDevice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAdapter* \[ de\]
</dt> <dd>

Tipo: **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***

Puntero al adaptador de pantalla (consulte la interfaz [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) ) al crear un dispositivo de hardware; de lo contrario, establezca este parámetro en **null**. Si se especifica **null** al crear un dispositivo de hardware, Direct3D usará el primer adaptador enumerado por la interfaz [**IDXGIFactory**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) .

</dd> <dt>

*DriverType* \[ de\]
</dt> <dd>

Tipo: **[ **\_ \_ tipo de controlador D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**

El tipo de controlador de dispositivo (vea la enumeración del [**\_ \_ tipo de controlador D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) ). El tipo de controlador determina el tipo de dispositivo que va a crear.

</dd> <dt>

*Software* \[ de de\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Identificador de un módulo cargado que implementa un controlador de software (como D3D10Ref.dll). Para obtener un identificador, llame a la función [GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) .

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Marcas de creación de dispositivos (consulte [**D3D10 \_ Create \_ Device \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) Enumeration) que habilitan las [capas de API](d3d10-graphics-programming-guide-api-features-layers.md). Estas marcas pueden ser OR bit a bit.

</dd> <dt>

*ppDevice* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Dirección de un puntero al dispositivo creado (vea la interfaz [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) ).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Esta función devuelve uno de los siguientes [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Esta función intenta crear el mejor dispositivo para el hardware. En primer lugar, la función intenta crear un dispositivo 10,1. Si no se puede crear un dispositivo 10,1, la función intenta crear un dispositivo 10,0. Si ninguno de los dispositivos se crea correctamente, la función devuelve E \_ Fail.

Si su aplicación solo necesita crear un dispositivo 10,1 o un dispositivo 10,0, use las siguientes funciones en su lugar:

-   Use la función [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) para crear solo un dispositivo Direct3D 10,0.
-   Use la función [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) para crear solo un dispositivo Direct3D 10,1.
-   Use la función [**D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md) para obtener un puntero de interfaz [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) de un puntero de interfaz [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) .

Un dispositivo Direct3D 10,1 solo se puede crear en equipos que ejecutan Windows Vista Service Pack 1 o posterior y con hardware compatible con Direct3D 10,1 instalado. Sin embargo, es válido llamar a esta función en equipos que ejecutan cualquier versión de Windows que tenga instalado el archivo DLL D3DX10.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de De uso general](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
