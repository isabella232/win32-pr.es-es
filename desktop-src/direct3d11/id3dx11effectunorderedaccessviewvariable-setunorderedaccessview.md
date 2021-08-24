---
title: Método ID3DX11EffectUnorderedAccessViewVariable SetUnorderedAccessView (D3dx11effect.h)
description: Establezca una vista unordered-access-view.
ms.assetid: a147879c-c5cf-4453-b27f-8716cb33962b
keywords:
- Método SetUnorderedAccessView Direct3D 11
- Método SetUnorderedAccessView Direct3D 11 , ID3DX11EffectUnorderedAccessViewVariable (interfaz)
- Interfaz ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, método SetUnorderedAccessView
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.SetUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d95dc15b0b79475cf7b8a731df291c73cb193db44fdc5bb917606dd916d6757
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565745"
---
# <a name="id3dx11effectunorderedaccessviewvariablesetunorderedaccessview-method"></a>Método ID3DX11EffectUnorderedAccessViewVariable::SetUnorderedAccessView

Establezca una vista unordered-access-view.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetUnorderedAccessView(
   ID3D11UnorderedAccessView *pResource
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pResource* 
</dt> <dd>

Tipo: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\***

Puntero a [**un id3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview).

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

[ID3DX11EffectUnorderedAccessViewVariable](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

 





