---
title: Método ID3DX11EffectSamplerVariable SetSampler (D3dx11effect.h)
description: Establezca el estado del muestreador.
ms.assetid: 1826923d-d770-4d79-818a-a42a279f0a8c
keywords:
- Método SetSampler Direct3D 11
- Método SetSampler Direct3D 11, interfaz ID3DX11EffectSamplerVariable
- Interfaz ID3DX11EffectSamplerVariable Direct3D 11, método SetSampler
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
ms.openlocfilehash: a4667b8261b46b1ecb1732c1ecc77efcf93d327426f0ea20f6c7710e94ed825e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791945"
---
# <a name="id3dx11effectsamplervariablesetsampler-method"></a>Método ID3DX11EffectSamplerVariable::SetSampler

Establezca el estado del muestreador.

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

Indexar en una matriz de interfaces sampler. Si solo hay una interfaz sampler, use 0.

</dd> <dt>

*pSampler* 
</dt> <dd>

Tipo: **[ **ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\***

Puntero a una [**interfaz ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate) que contiene el estado del sampler.

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

[ID3DX11EffectSamplerVariable](id3dx11effectsamplervariable.md)
</dt> </dl>

 

