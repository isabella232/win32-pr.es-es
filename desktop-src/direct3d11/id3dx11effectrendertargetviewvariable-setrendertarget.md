---
title: Método ID3DX11EffectRenderTargetViewVariable SetRenderTarget (D3dx11effect. h)
description: Establezca un destino de representación.
ms.assetid: caac7190-4f58-4a8e-9764-b6120ac14856
keywords:
- Método SetRenderTarget Direct3D 11
- Método SetRenderTarget Direct3D 11, interfaz ID3DX11EffectRenderTargetViewVariable
- Interfaz ID3DX11EffectRenderTargetViewVariable Direct3D 11, método SetRenderTarget
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
ms.openlocfilehash: eb53f0dff19fcd8990575dc9b305b0fb2f7e149b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914826"
---
# <a name="id3dx11effectrendertargetviewvariablesetrendertarget-method"></a>ID3DX11EffectRenderTargetViewVariable:: SetRenderTarget (método)

Establezca un destino de representación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetRenderTarget(
   ID3D11RenderTargetView *pResource
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*código fuente* 
</dt> <dd>

Tipo: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\***

Puntero a una interfaz de presentación-destino-vista. Vea [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).

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

[ID3DX11EffectRenderTargetViewVariable](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

 





