---
title: Método ID3DX11EffectBlendVariable SetBlendState (D3dx11effect.h)
description: Establece el estado de mezcla de un efecto.
ms.assetid: 46100721-65a3-46de-aa22-3e7e2fb7b960
keywords:
- Método SetBlendState Direct3D 11
- Método SetBlendState Direct3D 11 , interfaz ID3DX11EffectBlendVariable
- Interfaz ID3DX11EffectBlendVariable Direct3D 11, método SetBlendState
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.SetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a8f945faaf7f07846ea58b91378bbf2e6c06eeb1c3d0d041a6e0a71e2e9ea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046503"
---
# <a name="id3dx11effectblendvariablesetblendstate-method"></a>Método ID3DX11EffectBlendVariable::SetBlendState

Establece el estado de mezcla de un efecto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetBlendState(
   UINT             Index,
   ID3D11BlendState *pBlendState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indexe en una matriz de interfaces de estado de mezcla. Si solo hay una interfaz de estado de mezcla, use 0.

</dd> <dt>

*pBlendState* 
</dt> <dd>

Tipo: **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\***

Puntero a una [**interfaz ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate) que contiene el estado de mezcla que se establecerá.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Observaciones

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectBlendVariable](id3dx11effectblendvariable.md)
</dt> </dl>

 

