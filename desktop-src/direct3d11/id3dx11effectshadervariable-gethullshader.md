---
title: Método ID3DX11EffectShaderVariable GetHullShader (D3dx11effect. h)
description: Obtener un sombreador de casco.
ms.assetid: 18b2a8fc-2c53-4858-9aaa-00d0dc86adee
keywords:
- Método GetHullShader Direct3D 11
- Método GetHullShader Direct3D 11, interfaz ID3DX11EffectShaderVariable
- Interfaz ID3DX11EffectShaderVariable Direct3D 11, método GetHullShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetHullShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7eac8e6e095eb1ddbba93d68bec87e85e0c4e22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998755"
---
# <a name="id3dx11effectshadervariablegethullshader-method"></a>ID3DX11EffectShaderVariable:: GetHullShader (método)

Obtener un sombreador de casco.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetHullShader(
   UINT             ShaderIndex,
   ID3D11HullShader **ppPS
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Índice del sombreador.

</dd> <dt>

*ppPS* 
</dt> <dd>

Tipo: **[ **ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader)\*\***

Un puntero a un puntero [**ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader) que se establecerá en el sombreador de casco en la devolución.

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

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

