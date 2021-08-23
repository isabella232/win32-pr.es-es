---
title: Método ID3DX11EffectPass GetVertexShaderDesc (D3dx11effect.h)
description: Obtiene una descripción del sombreador de vértices.
ms.assetid: 7e02a438-2ff4-4e32-bc16-d112aafa57cb
keywords:
- Método GetVertexShaderDesc Direct3D 11
- Método GetVertexShaderDesc Direct3D 11, interfaz ID3DX11EffectPass
- Interfaz ID3DX11EffectPass Direct3D 11, método GetVertexShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetVertexShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7942fc1f8202065ac904223693c70b4dc8ea70bf3421158a08bad253acc67567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045979"
---
# <a name="id3dx11effectpassgetvertexshaderdesc-method"></a>Método ID3DX11EffectPass::GetVertexShaderDesc

Obtiene una descripción del sombreador de vértices.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetVertexShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ PASS \_ SHADER \_ DESC**](d3dx11-pass-shader-desc.md)\***

Puntero a una descripción del sombreador de vértices (vea [**D3DX11 \_ PASS \_ SHADER \_ DESC).**](d3dx11-pass-shader-desc.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Un paso de efecto puede contener asignaciones de estado de representación y asignaciones de objetos de sombreador.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





