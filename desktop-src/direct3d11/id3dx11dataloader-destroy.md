---
title: Método Destroy de ID3DX11DataLoader (D3DX11core.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Destruye el cargador una vez completado un elemento de trabajo.
ms.assetid: 5d86c4ad-3eb6-421f-bb77-c88e8f5b42bb
keywords:
- Destruir el método Direct3D 11
- Destruir el método Direct3D 11, interfaz ID3DX11DataLoader
- ID3DX11DataLoader interface Direct3D 11 , Destroy method
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Destroy
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 769b6531f530f325e288eb7fa5cc054a80ccac70f0d2930ec0b42e6ff033b6be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633025"
---
# <a name="id3dx11dataloaderdestroy-method"></a>Método ID3DX11DataLoader::D estroy

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

Destruye el cargador una vez completado un elemento de trabajo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Destroy();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno [de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Este método lo usa una interfaz [**ID3DX11ThreadPump**](id3dx11threadpump.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11DataLoader](id3dx11dataloader.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





