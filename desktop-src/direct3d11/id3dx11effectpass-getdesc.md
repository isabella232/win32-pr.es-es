---
title: Método Id3DX11EffectPass GetDesc (D3dx11effect.h)
description: Obtenga una descripción de paso.
ms.assetid: 423766be-96b2-4038-834e-34125789e8b1
keywords:
- Método GetDesc Direct3D 11
- Método GetDesc Direct3D 11, interfaz ID3DX11EffectPass
- Interfaz ID3DX11EffectPass direct3D 11, método GetDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfd75b5b23e253715af33c712fe957ae057b681f715a60fa37d4451c3fc76232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535071"
---
# <a name="id3dx11effectpassgetdesc-method"></a>Método ID3DX11EffectPass::GetDesc

Obtenga una descripción de paso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDesc(
   D3DX11_PASS_DESC *pDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ PASS \_ DESC**](d3dx11-pass-desc.md)\***

Puntero a una descripción de paso (vea [**D3DX11 \_ PASS \_ DESC**](d3dx11-pass-desc.md)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Un paso es un bloque de código que establece el estado de representación y los sombreadores (que a su vez establece búferes constantes, muestreadores y texturas). Una técnica de efecto contiene uno o varios pases.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





