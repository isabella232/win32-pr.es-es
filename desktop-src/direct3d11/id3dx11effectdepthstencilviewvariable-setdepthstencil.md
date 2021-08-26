---
title: Método ID3DX11EffectDepthStencilViewVariable SetDepthStencil (D3dx11effect.h)
description: Establezca un recurso depth-stencil-view.
ms.assetid: 35cbcd3b-6fc8-448d-a82e-724f91038d07
keywords:
- Método SetDepthStencil Direct3D 11
- Método SetDepthStencil Direct3D 11 , interfaz ID3DX11EffectDepthStencilViewVariable
- ID3DX11EffectDepthStencilViewVariable interface Direct3D 11 , SetDepthStencil method
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.SetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae1e8b984bb15e083360ef99036549c534d8e047a2375ad0b0a6e5469b9191c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069685"
---
# <a name="id3dx11effectdepthstencilviewvariablesetdepthstencil-method"></a>Método ID3DX11EffectDepthStencilViewVariable::SetDepthStencil

Establezca un recurso depth-stencil-view.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDepthStencil(
   ID3D11DepthStencilView *pResource
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pResource* 
</dt> <dd>

Tipo: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\***

Puntero a una interfaz de vista de galería de símbolos de profundidad. Vea [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).

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

[ID3DX11EffectDepthStencilViewVariable](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

 





