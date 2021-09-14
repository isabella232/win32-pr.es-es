---
title: Método ID3DX11EffectSamplerVariable GetBackingStore (D3dx11effect.h)
description: Obtiene un puntero a una variable que contiene el estado del muestreador.
ms.assetid: b188fb86-f54b-481e-9110-7b8af70ff303
keywords:
- Método GetBackingStore Direct3D 11
- Método GetBackingStore Direct3D 11, interfaz ID3DX11EffectSamplerVariable
- Interfaz ID3DX11EffectSamplerVariable Direct3D 11 , método GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03f2d6ac3035d1dd2fd3aee8950135d7b4481862
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160478"
---
# <a name="id3dx11effectsamplervariablegetbackingstore-method"></a>Método ID3DX11EffectSamplerVariable::GetBackingStore

Obtiene un puntero a una variable que contiene el estado del muestreador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetBackingStore(
   UINT               Index,
   D3D11_SAMPLER_DESC *pSamplerDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indexe en una matriz de descripciones de sampler. Si solo hay una variable sampler en el efecto, use 0.

</dd> <dt>

*pSamplerDesc* 
</dt> <dd>

Tipo: **[ **D3D11 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)\***

Puntero a una descripción del muestreador (vea [**D3D11 \_ SAMPLER \_ DESC).**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Observaciones

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX11EffectSamplerVariable](id3dx11effectsamplervariable.md)
</dt> </dl>

 

