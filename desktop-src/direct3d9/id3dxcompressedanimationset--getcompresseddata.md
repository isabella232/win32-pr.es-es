---
description: Obtiene el búfer de datos que almacena los datos de animación de fotogramas clave comprimidos.
ms.assetid: cb42a4c8-6420-4694-9921-0d36cfe960e5
title: 'ID3DXCompressedAnimationSet:: GetCompressedData (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCompressedData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7907daf5db2d03afca310a630f6aeb2dc16c4f22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678800"
---
# <a name="id3dxcompressedanimationsetgetcompresseddata-method"></a>ID3DXCompressedAnimationSet:: GetCompressedData (método)

Obtiene el búfer de datos que almacena los datos de animación de fotogramas clave comprimidos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCompressedData(
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppCompressedData* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero al búfer de datos [**ID3DXBuffer**](id3dxbuffer.md) que recibe los datos de animación de fotogramas clave comprimidos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXCompressedAnimationSet](id3dxcompressedanimationset.md)
</dt> </dl>

 

 




