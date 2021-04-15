---
title: Método ID3DX11EffectShaderVariable GetOutputSignatureElementDesc (D3dx11effect. h)
description: Obtiene una descripción de la firma de salida.
ms.assetid: 05f43a57-18fa-4be7-814e-ffbe53837cab
keywords:
- Método GetOutputSignatureElementDesc Direct3D 11
- Método GetOutputSignatureElementDesc Direct3D 11, interfaz ID3DX11EffectShaderVariable
- Interfaz ID3DX11EffectShaderVariable Direct3D 11, método GetOutputSignatureElementDesc
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998664"
---
# <a name="id3dx11effectshadervariablegetoutputsignatureelementdesc-method"></a>ID3DX11EffectShaderVariable:: GetOutputSignatureElementDesc (método)

Obtiene una descripción de la firma de salida.

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

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Índice de sombreador basado en cero.

</dd> <dt>

*Element* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Índice de elemento basado en cero.

</dd> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **\_ parámetro de firma D3D11 \_ \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***

Un puntero a una descripción de parámetro (vea [**D3D11 \_ Signature \_ Parameter \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Un efecto contiene uno o varios sombreadores; cada sombreador tiene una firma de entrada y salida; cada firma contiene uno o más elementos (o parámetros). El índice del sombreador identifica el sombreador y el índice del elemento identifica el elemento (o parámetro) de la firma del sombreador.

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

 

