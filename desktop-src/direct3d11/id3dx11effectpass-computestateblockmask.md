---
title: Método ID3DX11EffectPass ComputeStateBlockMask (D3dx11effect.h)
description: Genere una máscara para permitir o evitar cambios de estado.
ms.assetid: 584be931-0e22-43e6-b852-f0d2ab050bdd
keywords:
- Método ComputeStateBlockMask Direct3D 11
- Método ComputeStateBlockMask Direct3D 11, interfaz ID3DX11EffectPass
- Interfaz ID3DX11EffectPass Direct3D 11, método ComputeStateBlockMask
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17198c076d200631142207189059ada425e9ec1ddf6e3c8a8d40499e40aa21a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535061"
---
# <a name="id3dx11effectpasscomputestateblockmask-method"></a>Método ID3DX11EffectPass::ComputeStateBlockMask

Genere una máscara para permitir o evitar cambios de estado.

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
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





