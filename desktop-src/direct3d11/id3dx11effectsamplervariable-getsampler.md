---
title: Método ID3DX11EffectSamplerVariable GetSampler (D3dx11effect.h)
description: Obtenga un puntero a una interfaz sampler.
ms.assetid: ac2a05f1-e3ca-4ebf-b655-34133c4e50ac
keywords:
- Método GetSampler Direct3D 11
- Método GetSampler Direct3D 11, interfaz ID3DX11EffectSamplerVariable
- Interfaz ID3DX11EffectSamplerVariable direct3D 11, método GetSampler
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.GetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfc9c400f3596d380f5e671eaa04f4e4340bde385230f331e3e2fdc7ee1a92f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045833"
---
# <a name="id3dx11effectsamplervariablegetsampler-method"></a>Método ID3DX11EffectSamplerVariable::GetSampler

Obtenga un puntero a una interfaz sampler.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSampler(
   UINT               Index,
   ID3D11SamplerState **ppSampler
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indexe en una matriz de interfaces sampler. Si solo hay una interfaz sampler, use 0.

</dd> <dt>

*ppSampler* 
</dt> <dd>

Tipo: **[ **ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\*\***

Dirección de un puntero a una interfaz sampler (vea [**ID3D11SamplerState).**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)

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

[ID3DX11EffectSamplerVariable](id3dx11effectsamplervariable.md)
</dt> </dl>

 

