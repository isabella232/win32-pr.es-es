---
title: Método ID3DX11EffectShaderVariable GetPatchConstantSignatureElementDesc (D3dx11effect.h)
description: Obtiene una descripción de firma de constante de revisión.
ms.assetid: 72a86cf6-ace2-4306-ac5c-37d888c087f7
keywords:
- Método GetPatchConstantSignatureElementDesc Direct3D 11
- Método GetPatchConstantSignatureElementDesc Direct3D 11 e ID3DX11EffectShaderVariable
- Interfaz ID3DX11EffectShaderVariable Direct3D 11 , método GetPatchConstantSignatureElementDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetPatchConstantSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4fcbc8f7c1bc34b0da42dd08c255a04a6d2fc83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127581245"
---
# <a name="id3dx11effectshadervariablegetpatchconstantsignatureelementdesc-method"></a>Método ID3DX11EffectShaderVariable::GetPatchConstantSignatureElementDesc

Obtiene una descripción de firma de constante de revisión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPatchConstantSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Índice de sombreador de base cero.

</dd> <dt>

*Element* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Índice de elemento de base cero.

</dd> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3D11 \_ SIGNATURE \_ PARAMETER \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***

Puntero a una descripción de parámetro (vea [**D3D11 \_ SIGNATURE \_ PARAMETER \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Observaciones

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

