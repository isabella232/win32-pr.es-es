---
title: Método ID3DX11EffectDepthStencilVariable GetBackingStore (D3dx11effect.h)
description: Obtiene un puntero a una variable que contiene el estado de galería de símbolos de profundidad.
ms.assetid: 6aeed5ac-f0ee-4e8c-b87b-022f58c9094c
keywords:
- Método GetBackingStore Direct3D 11
- Método GetBackingStore Direct3D 11 , ID3DX11EffectDepthStencilVariable (interfaz)
- ID3DX11EffectDepthStencilVariable interface Direct3D 11 , Método GetBackingStore
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060828"
---
# <a name="id3dx11effectdepthstencilvariablegetbackingstore-method"></a>Método ID3DX11EffectDepthStencilVariable::GetBackingStore

Obtiene un puntero a una variable que contiene el estado de galería de símbolos de profundidad.

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

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indexe en una matriz de descripciones de estado de galería de símbolos de profundidad. Si solo hay una variable de galería de símbolos de profundidad en el efecto, use 0.

</dd> <dt>

*pDepthStencilDesc* 
</dt> <dd>

Tipo: **[ **D3D11 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)\***

Puntero a una descripción de estado de galería de símbolos de profundidad (vea [**D3D11 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Observaciones

Las variables de efecto se guardan en memoria en el almacén de respaldo; cuando se aplica una técnica, los valores de la tienda de respaldo se copian en el dispositivo. Los datos de almacenamiento de respaldo se pueden usar para volver a crear la variable cuando sea necesario.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX11EffectDepthStencilVariable](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

