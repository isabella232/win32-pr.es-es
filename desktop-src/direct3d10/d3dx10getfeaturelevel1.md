---
description: Obtiene un puntero de interfaz de dispositivo de Direct3D 10,1 de un puntero de interfaz de Direct3D 10,0.
ms.assetid: cf31a67f-0493-4e79-8e73-0297ab93bbae
title: Función D3DX10GetFeatureLevel1 (D3DX10Core. h)
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
ms.openlocfilehash: 817eb4dd68ce797da76c0609e2ead01a21b5b270
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707749"
---
# <a name="d3dx10getfeaturelevel1-function"></a>D3DX10GetFeatureLevel1 función)

Obtiene un puntero de interfaz de dispositivo de Direct3D 10,1 de un puntero de interfaz de Direct3D 10,0.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10GetFeatureLevel1(
  _In_  ID3D10Device  *pDevice,
  _Out_ ID3D10Device1 **ppDevice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Puntero al dispositivo Direct3D 10,0 (vea la interfaz [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) ).

</dd> <dt>

*ppDevice* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***

Puntero al dispositivo Direct3D 10,1 (vea la interfaz [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) ).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Esta función devuelve uno de los siguientes [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md). Si se puede adquirir una interfaz de dispositivo de Direct3D 10,1, esta función se ejecuta correctamente y pasa un puntero a la interfaz 10,1 mediante el parámetro *ppDevice* . Si no se puede adquirir una interfaz de dispositivo de Direct3D 10,1, esta función devuelve E \_ FAIL, y no devolverá nada para el parámetro *ppDevice* .

## <a name="remarks"></a>Observaciones

Para que esta función se realice correctamente, debe haber adquirido el puntero [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) proporcionado mediante una llamada a la función [**D3DX10CreateDevice**](d3dx10createdevice.md) , la función [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md) , la función [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) o la función [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) .

Solo puede crear un dispositivo Direct3D 10,1 en equipos que ejecuten Windows Vista Service Pack 1 o posterior y con el hardware compatible con Direct3D 10,1 instalado. Esta función devolverá E \_ producirá un error en cualquier equipo que no cumpla estos requisitos. Sin embargo, puede llamar a esta función en cualquier versión de Windows que tenga instalado el archivo DLL D3DX10.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de De uso general](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




