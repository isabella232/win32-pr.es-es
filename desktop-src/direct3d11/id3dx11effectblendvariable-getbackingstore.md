---
title: Método ID3DX11EffectBlendVariable GetBackingStore (D3dx11effect. h)
description: Obtiene un puntero a una variable de estado de mezcla.
ms.assetid: 809daaad-9bf0-48fb-ae91-f237c43db324
keywords:
- Método GetBackingStore Direct3D 11
- Método GetBackingStore Direct3D 11, interfaz ID3DX11EffectBlendVariable
- Interfaz ID3DX11EffectBlendVariable Direct3D 11, método GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0220481b58931edace2a5dfe7298d83f7bd1325
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280448"
---
# <a name="id3dx11effectblendvariablegetbackingstore-method"></a>ID3DX11EffectBlendVariable:: GetBackingStore (método)

Obtiene un puntero a una variable de estado de mezcla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetBackingStore(
   UINT             Index,
   D3D11_BLEND_DESC *pBlendDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Índice en una matriz de descripciones de estado de Blend. Si solo hay una variable de estado de mezcla en el efecto, use 0.

</dd> <dt>

*pBlendDesc* 
</dt> <dd>

Tipo: **[ **D3D11 \_ Blend \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)\***

Un puntero a una descripción del estado de Blend (vea [**D3D11 \_ Blend \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Las variables de efecto se guardan en la memoria de la memoria auxiliar. Cuando se aplica una técnica, los valores de la memoria auxiliar se copian en el dispositivo. Los datos de la memoria auxiliar se pueden usar para volver a crear la variable cuando sea necesario.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects. Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectBlendVariable](id3dx11effectblendvariable.md)
</dt> </dl>

 

