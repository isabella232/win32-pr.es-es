---
title: Método ID3DX11DataProcessor Destroy (D3DX11core.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para las aplicaciones de Windows Store. Destruye el procesador una vez completado un elemento de trabajo.
ms.assetid: 759641c0-ef86-42ee-88b9-3fcb7a171d86
keywords:
- Destruir el método Direct3D 11
- Método Destroy Direct3D 11 , id3DX11DataProcessor (interfaz)
- Id3DX11DataProcessor interface Direct3D 11 , Destroy method
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.Destroy
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0968ff090f01a27cb18d3fff0e6dbd499c05c95cd558a2eba805dd91a153c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632935"
---
# <a name="id3dx11dataprocessordestroy-method"></a>Id3DX11DataProcessor::D estroy (método)

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

Destruye el procesador una vez completado un elemento de trabajo.

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

[ID3DX11DataProcessor](id3dx11dataprocessor.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





