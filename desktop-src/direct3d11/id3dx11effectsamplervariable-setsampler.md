---
title: Método ID3DX11EffectSamplerVariable SetSampler (D3dx11effect.h)
description: Establezca el estado del sampler.
ms.assetid: 1826923d-d770-4d79-818a-a42a279f0a8c
keywords:
- Método SetSampler Direct3D 11
- Método SetSampler Direct3D 11, interfaz ID3DX11EffectSamplerVariable
- Interfaz ID3DX11EffectSamplerVariable direct3D 11, método SetSampler
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.SetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77a68adef00ac980b532e2fcd877e71eb63dc470
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160476"
---
# <a name="id3dx11effectsamplervariablesetsampler-method"></a>Método ID3DX11EffectSamplerVariable::SetSampler

Establezca el estado del sampler.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSampler(
   UINT               Index,
   ID3D11SamplerState *pSampler
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indexe en una matriz de interfaces sampler. Si solo hay una interfaz sampler, use 0.

</dd> <dt>

*pSampler* 
</dt> <dd>

Tipo: **[ **ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\***

Puntero a una [**interfaz ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate) que contiene el estado del sampler.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Observaciones

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX11EffectSamplerVariable](id3dx11effectsamplervariable.md)
</dt> </dl>

 

