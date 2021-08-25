---
title: Método ID3DX11EffectTechnique ComputeStateBlockMask (D3dx11effect.h)
description: Calcule una máscara de bloque de estado para permitir o evitar cambios de estado.
ms.assetid: 4fd6061d-6ca5-4e3f-b031-fae98f3de057
keywords:
- Método ComputeStateBlockMask Direct3D 11
- Método ComputeStateBlockMask Direct3D 11, interfaz ID3DX11EffectTechnique
- Interfaz ID3DX11EffectTechnique Direct3D 11, método ComputeStateBlockMask
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf7a221cd685eb31b068ae6144514adb70ffa42c654d9e1a3249db5302e0aa6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894765"
---
# <a name="id3dx11effecttechniquecomputestateblockmask-method"></a>Método ID3DX11EffectTechnique::ComputeStateBlockMask

Calcule una máscara de bloque de estado para permitir o evitar cambios de estado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStateBlockMask* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ STATE \_ BLOCK \_ MASK**](d3dx11-state-block-mask.md)\***

Puntero a una máscara de bloque de estado (vea [**D3DX11 \_ STATE \_ BLOCK \_ MASK**](d3dx11-state-block-mask.md)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

 





