---
title: Método ID3DX11DataProcessor CreateDeviceObject (D3DX11core. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Crea un objeto de dispositivo.
ms.assetid: 797d216b-2f54-4d24-aa97-04be0c71f909
keywords:
- Método CreateDeviceObject Direct3D 11
- Método CreateDeviceObject Direct3D 11, interfaz ID3DX11DataProcessor
- Interfaz ID3DX11DataProcessor Direct3D 11, método CreateDeviceObject
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.CreateDeviceObject
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ff178cec1830d1b0213af23a2a70654416d35e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362806"
---
# <a name="id3dx11dataprocessorcreatedeviceobject-method"></a>ID3DX11DataProcessor:: CreateDeviceObject (método)

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 

Crea un objeto de dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateDeviceObject(
  [out] void **ppDataObject
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppDataObject* \[ enuncia\]
</dt> <dd>

Tipo: **void \* \***

Dirección de un puntero al objeto de dispositivo creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Este método lo usa una [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11DataProcessor](id3dx11dataprocessor.md)
</dt> <dt>

[Interfaces de D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





