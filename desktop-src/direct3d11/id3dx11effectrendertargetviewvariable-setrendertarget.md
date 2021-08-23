---
title: Método ID3DX11EffectRenderTargetViewVariable SetRenderTarget (D3dx11effect.h)
description: Establezca un destino de representación.
ms.assetid: caac7190-4f58-4a8e-9764-b6120ac14856
keywords:
- Método SetRenderTarget Direct3D 11
- Método SetRenderTarget Direct3D 11 , interfaz ID3DX11EffectRenderTargetViewVariable
- Interfaz ID3DX11EffectRenderTargetViewVariable direct3D 11, método SetRenderTarget
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.SetRenderTarget
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69bd36ddab704ab7ac78d78e7e7cf0c2262794df76730bc6f9019662c292abbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045854"
---
# <a name="id3dx11effectrendertargetviewvariablesetrendertarget-method"></a>Método ID3DX11EffectRenderTargetViewVariable::SetRenderTarget

Establezca un destino de representación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetRenderTarget(
   ID3D11RenderTargetView *pResource
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pResource* 
</dt> <dd>

Tipo: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\***

Puntero a una interfaz render-target-view. Vea [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).

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

[ID3DX11EffectRenderTargetViewVariable](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

 





