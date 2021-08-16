---
title: Método ID3DX11EffectShaderResourceVariable SetResource (D3dx11effect.h)
description: Establezca un recurso de sombreador.
ms.assetid: f85c33ff-dc00-4421-939c-74f9317faadc
keywords:
- Método SetResource Direct3D 11
- Método SetResource Direct3D 11, interfaz ID3DX11EffectShaderResourceVariable
- Interfaz ID3DX11EffectShaderResourceVariable Direct3D 11, método SetResource
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.SetResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf0db2db1886298633ba70fa9af6ce1d475b5c511487b35e65d20373f8282f3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533443"
---
# <a name="id3dx11effectshaderresourcevariablesetresource-method"></a>Método ID3DX11EffectShaderResourceVariable::SetResource

Establezca un recurso de sombreador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetResource(
   ID3D11ShaderResourceView *pResource
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pResource* 
</dt> <dd>

Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***

Dirección de un puntero a una interfaz shader-resource-view. Vea [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX11EffectShaderResourceVariable](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

 





