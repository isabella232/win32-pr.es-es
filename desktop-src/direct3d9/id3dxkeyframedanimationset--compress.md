---
description: Transforma las animaciones de una animación establecida en un formato comprimido y devuelve un puntero al búfer que almacena los datos comprimidos.
ms.assetid: b70b6dfb-545f-4309-ab72-9543c3c48fc4
title: 'Método ID3DXKeyframedAnimationSet:: compress (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.Compress
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd3a278760f2598df52d251a9e3558a72f954ceb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708078"
---
# <a name="id3dxkeyframedanimationsetcompress-method"></a>ID3DXKeyframedAnimationSet:: compress (método)

Transforma las animaciones de una animación establecida en un formato comprimido y devuelve un puntero al búfer que almacena los datos comprimidos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Compress(
  [in]  DWORD        Flags,
  [in]  FLOAT        Lossiness,
  [in]  LPD3DXFRAME  pHierarchy,
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Uno de los valores de las [**\_ marcas D3DXCOMPRESSION**](./d3dxcompression-flags.md) que definen el modo de compresión utilizado para almacenar los datos de conjuntos de animación comprimidos. D3DXCOMPRESS \_ default es el único valor que se admite actualmente.

</dd> <dt>

*Disminución* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Proporción de pérdida de compresión deseada, en el intervalo de 0 a 1.

</dd> <dt>

*pHierarchy* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**

Puntero a una jerarquía de fotogramas de transformación [**D3DXFRAME**](d3dxframe.md) . Puede ser **null**.

</dd> <dt>

*ppCompressedData* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero al conjunto de animaciones comprimidas de [**ID3DXBuffer**](id3dxbuffer.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
