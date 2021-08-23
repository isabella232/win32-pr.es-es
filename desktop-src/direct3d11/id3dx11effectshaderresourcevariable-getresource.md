---
title: Método ID3DX11EffectShaderResourceVariable GetResource (D3dx11effect.h)
description: Obtiene un recurso de sombreador.
ms.assetid: 7c56aba0-ce60-4b50-9c1a-802bf1d73c6b
keywords:
- Método GetResource Direct3D 11
- Método GetResource Direct3D 11, interfaz ID3DX11EffectShaderResourceVariable
- Interfaz ID3DX11EffectShaderResourceVariable Direct3D 11, método GetResource
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.GetResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a11cf0878078ac3152f23a088290f4dd1d046f516dae50e77d22cb7e5ea70a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533577"
---
# <a name="id3dx11effectshaderresourcevariablegetresource-method"></a>Método ID3DX11EffectShaderResourceVariable::GetResource

Obtiene un recurso de sombreador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetResource(
   ID3D11ShaderResourceView **ppResource
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppResource* 
</dt> <dd>

Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***

Dirección de un puntero a una interfaz shader-resource-view. Vea [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectShaderResourceVariable](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

 





