---
title: Método ID3DX11EffectShaderVariable GetOutputSignatureElementDesc (D3dx11effect.h)
description: Obtenga una descripción de la firma de salida.
ms.assetid: 05f43a57-18fa-4be7-814e-ffbe53837cab
keywords:
- Método GetOutputSignatureElementDesc direct3D 11
- Método GetOutputSignatureElementDesc Direct3D 11 , interfaz ID3DX11EffectShaderVariable
- Interfaz ID3DX11EffectShaderVariable direct3D 11 , método GetOutputSignatureElementDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetOutputSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29545754be560a3a7710adf23963566a324d8a3f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127581248"
---
# <a name="id3dx11effectshadervariablegetoutputsignatureelementdesc-method"></a>Método ID3DX11EffectShaderVariable::GetOutputSignatureElementDesc

Obtenga una descripción de la firma de salida.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetOutputSignatureElementDesc(
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

Un efecto contiene uno o varios sombreadores; cada sombreador tiene una firma de entrada y salida; cada firma contiene uno o varios elementos (o parámetros). El índice de sombreador identifica el sombreador y el índice del elemento identifica el elemento (o parámetro) en la firma del sombreador.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

