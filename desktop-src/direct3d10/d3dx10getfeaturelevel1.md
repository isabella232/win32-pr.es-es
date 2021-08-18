---
description: Obtenga un puntero de interfaz de dispositivo Direct3D 10.1 a partir de un puntero de interfaz direct3D 10.0.
ms.assetid: cf31a67f-0493-4e79-8e73-0297ab93bbae
title: Función D3DX10GetFeatureLevel1 (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetFeatureLevel1
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: c6511e0d3963e21f8950529b32cf8c3b414cc00b0625b97b2a9d569d1523c326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753175"
---
# <a name="d3dx10getfeaturelevel1-function"></a>Función D3DX10GetFeatureLevel1

Obtenga un puntero de interfaz de dispositivo Direct3D 10.1 a partir de un puntero de interfaz direct3D 10.0.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10GetFeatureLevel1(
  _In_  ID3D10Device  *pDevice,
  _Out_ ID3D10Device1 **ppDevice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Puntero al dispositivo Direct3D 10.0 (consulte la [**interfaz ID3D10Device).**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)

</dd> <dt>

*ppDevice* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***

Puntero al dispositivo Direct3D 10.1 (vea la [**interfaz ID3D10Device1).**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Esta función devuelve uno de los siguientes códigos de retorno [de Direct3D 10.](d3d10-graphics-reference-returnvalues.md) Si se puede adquirir una interfaz de dispositivo Direct3D 10.1, esta función se realiza correctamente y pasa un puntero a la interfaz 10.1 mediante el *parámetro ppDevice.* Si no se puede adquirir una interfaz de dispositivo Direct3D 10.1, esta función devuelve E FAIL y no devolverá nada para \_ el *parámetro ppDevice.*

## <a name="remarks"></a>Comentarios

Para que esta función se haga correctamente, debe haber adquirido el puntero [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) proporcionado mediante una llamada a la función [**D3DX10CreateDevice,**](d3dx10createdevice.md) la función [**D3DX10CreateDeviceAndSwapChain,**](d3dx10createdeviceandswapchain.md) la función [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) o la función [**D3D10CreateDeviceAndSwapChain1.**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1)

Solo puede crear un dispositivo Direct3D 10.1 en equipos que ejecutan Windows Vista Service Pack 1 o posterior, y con hardware compatible con Direct3D 10.1 instalado. Esta función devolverá E \_ FAIL en cualquier equipo que no cumple estos requisitos. Sin embargo, puede llamar a esta función en cualquier versión Windows que tenga instalado el archivo DLL D3DX10.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Core.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[De uso general Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




