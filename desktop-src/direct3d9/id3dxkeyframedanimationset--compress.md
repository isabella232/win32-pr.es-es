---
description: Transforma las animaciones de un conjunto de animación en un formato comprimido y devuelve un puntero al búfer que almacena los datos comprimidos.
ms.assetid: b70b6dfb-545f-4309-ab72-9543c3c48fc4
title: Método ID3DXKeyframedAnimationSet::Compress (D3dx9anim.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360855"
---
# <a name="id3dxkeyframedanimationsetcompress-method"></a>Método ID3DXKeyframedAnimationSet::Compress

Transforma las animaciones de un conjunto de animación en un formato comprimido y devuelve un puntero al búfer que almacena los datos comprimidos.

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

*Marcas* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Uno de los [**valores D3DXCOMPRESSION \_ FLAGS**](./d3dxcompression-flags.md) que definen el modo de compresión utilizado para almacenar datos comprimidos del conjunto de animaciones. D3DXCOMPRESS \_ DEFAULT es el único valor admitido actualmente.

</dd> <dt>

*Pérdida* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Relación de pérdida de compresión deseada, en el intervalo de 0 a 1.

</dd> <dt>

*pHierarchy* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**

Puntero a una [**jerarquía de marco de transformación D3DXFRAME.**](d3dxframe.md) Puede ser **NULL.**

</dd> <dt>

*ppCompressedData* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero al conjunto de [**animación comprimida ID3DXBuffer.**](id3dxbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
