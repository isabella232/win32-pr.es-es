---
title: Función D3DX11UnsetAllDeviceObjects (D3DX11core. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar el método ID3D11DeviceContext ClearState.
ms.assetid: 0e52bbca-f171-477f-89b0-ba56a2cfa096
keywords:
- Función D3DX11UnsetAllDeviceObjects Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11UnsetAllDeviceObjects
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8ac7e33bfef7f8470f616ac07b3aa90463f3f3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362667"
---
# <a name="d3dx11unsetalldeviceobjects-function"></a>D3DX11UnsetAllDeviceObjects función)

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 

> [!Note]  
> En lugar de usar esta función, se recomienda usar el método [**ID3D11DeviceContext:: ClearState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate) .

 

Quita todos los recursos del dispositivo estableciendo sus punteros en **null**. Se debe llamar a este método durante el cierre de la aplicación. Ayuda a garantizar que cuando se liberan todos los recursos que no están enlazados al dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11UnsetAllDeviceObjects(
  _In_ ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContext* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Puntero a un objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





