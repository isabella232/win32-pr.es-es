---
title: Método ID3DX11EffectDepthStencilViewVariable GetDepthStencil (D3dx11effect.h)
description: Obtenga un recurso depth-stencil-view.
ms.assetid: 7d94d98b-7070-41ee-9a9d-fe848f8914f2
keywords:
- Método GetDepthStencil Direct3D 11
- Método GetDepthStencil Direct3D 11 , interfaz ID3DX11EffectDepthStencilViewVariable
- ID3DX11EffectDepthStencilViewVariable interface Direct3D 11 , GetDepthStencil method
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.GetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49206f051922982ac77265e68fa3d7b7397d1348
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060820"
---
# <a name="id3dx11effectdepthstencilviewvariablegetdepthstencil-method"></a>Método ID3DX11EffectDepthStencilViewVariable::GetDepthStencil

Obtenga un recurso depth-stencil-view.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDepthStencil(
   ID3D11DepthStencilView **ppResource
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppResource* 
</dt> <dd>

Tipo: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***

Dirección de un puntero a una interfaz de vista de galería de símbolos de profundidad. Vea [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).

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

[ID3DX11EffectDepthStencilViewVariable](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

 





