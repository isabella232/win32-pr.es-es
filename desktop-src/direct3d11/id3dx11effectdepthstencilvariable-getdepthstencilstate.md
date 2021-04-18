---
title: Método ID3DX11EffectDepthStencilVariable GetDepthStencilState (D3dx11effect. h)
description: Obtiene un puntero a una interfaz de estarcido de profundidad.
ms.assetid: 3e8f7fc6-960c-45f5-9276-9aa2a5e7a6c9
keywords:
- Método GetDepthStencilState Direct3D 11
- Método GetDepthStencilState Direct3D 11, interfaz ID3DX11EffectDepthStencilVariable
- Interfaz ID3DX11EffectDepthStencilVariable Direct3D 11, método GetDepthStencilState
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.GetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9276c7a126d5441361a4d449c4ee2ece70d995
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987132"
---
# <a name="id3dx11effectdepthstencilvariablegetdepthstencilstate-method"></a>ID3DX11EffectDepthStencilVariable:: GetDepthStencilState (método)

Obtiene un puntero a una interfaz de estarcido de profundidad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDepthStencilState(
   UINT                    Index,
   ID3D11DepthStencilState **ppDepthStencilState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Índice en una matriz de interfaces de estarcido de profundidad. Si solo hay una interfaz de estarcido de profundidad, use 0.

</dd> <dt>

*ppDepthStencilState* 
</dt> <dd>

Tipo: **[ **ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\*\***

La dirección de un puntero a una interfaz de estado de mezcla (vea [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)).

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

[ID3DX11EffectDepthStencilVariable](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

