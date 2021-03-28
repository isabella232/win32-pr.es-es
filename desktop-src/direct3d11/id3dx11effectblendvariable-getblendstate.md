---
title: Método ID3DX11EffectBlendVariable GetBlendState (D3dx11effect. h)
description: Obtiene un puntero a una interfaz de estado de mezcla.
ms.assetid: ab4ee765-b5ad-4dc3-9b00-48052528d3bd
keywords:
- Método GetBlendState Direct3D 11
- Método GetBlendState Direct3D 11, interfaz ID3DX11EffectBlendVariable
- Interfaz ID3DX11EffectBlendVariable Direct3D 11, método GetBlendState
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.GetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48092b496fa8a38be7c9dd8aea67a26e8b56f4f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362704"
---
# <a name="id3dx11effectblendvariablegetblendstate-method"></a>ID3DX11EffectBlendVariable:: GetBlendState (método)

Obtiene un puntero a una interfaz de estado de mezcla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetBlendState(
   UINT             Index,
   ID3D11BlendState **ppBlendState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Índice en una matriz de interfaces de estado de mezcla. Si solo hay una interfaz de estado de mezcla, use 0.

</dd> <dt>

*ppBlendState* 
</dt> <dd>

Tipo: **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\*\***

La dirección de un puntero a una interfaz de estado de mezcla (vea [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

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

 

