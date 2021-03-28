---
title: Método ID3DX11EffectDepthStencilVariable GetBackingStore (D3dx11effect. h)
description: Obtiene un puntero a una variable que contiene el estado de la galería de símbolos de profundidad.
ms.assetid: 6aeed5ac-f0ee-4e8c-b87b-022f58c9094c
keywords:
- Método GetBackingStore Direct3D 11
- Método GetBackingStore Direct3D 11, interfaz ID3DX11EffectDepthStencilVariable
- Interfaz ID3DX11EffectDepthStencilVariable Direct3D 11, método GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9335817b9c954958c97294a88291f83bf0e967d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986982"
---
# <a name="id3dx11effectdepthstencilvariablegetbackingstore-method"></a>ID3DX11EffectDepthStencilVariable:: GetBackingStore (método)

Obtiene un puntero a una variable que contiene el estado de la galería de símbolos de profundidad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetBackingStore(
   UINT                     Index,
   D3D11_DEPTH_STENCIL_DESC *pDepthStencilDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Índice en una matriz de descripciones de estado de estarcido de profundidad. Si solo hay una variable de estarcido de profundidad en el efecto, use 0.

</dd> <dt>

*pDepthStencilDesc* 
</dt> <dd>

Tipo: D3D11 de la **[ **\_ Galería de \_ símbolos \_ de profundidad**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)\***

Un puntero a una descripción del estado de la galería de símbolos de profundidad (consulte [**D3D11 \_ Depth \_ estarcido \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).

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

[ID3DX11EffectDepthStencilVariable](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

