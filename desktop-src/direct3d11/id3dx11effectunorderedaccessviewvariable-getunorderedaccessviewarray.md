---
title: Método ID3DX11EffectUnorderedAccessViewVariable GetUnorderedAccessViewArray (D3dx11effect.h)
description: Obtiene una matriz de vistas unordered-access-views.
ms.assetid: 38f838bb-cdcb-43c2-8b98-a188f479e93d
keywords:
- Método GetUnorderedAccessViewArray Direct3D 11
- Método GetUnorderedAccessViewArray Direct3D 11 , interfaz ID3DX11EffectUnorderedAccessViewVariable
- Interfaz ID3DX11EffectUnorderedAccessViewVariable Direct3D 11 , Método GetUnorderedAccessViewArray
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.GetUnorderedAccessViewArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84f38e55762996324b6d8fc53a093cef7759f136243faec7d78e5b568977a0f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532106"
---
# <a name="id3dx11effectunorderedaccessviewvariablegetunorderedaccessviewarray-method"></a>Método ID3DX11EffectUnorderedAccessViewVariable::GetUnorderedAccessViewArray

Obtiene una matriz de vistas unordered-access-views.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetUnorderedAccessViewArray(
   ID3D11UnorderedAccessView **ppResources,
   UINT                      Offset,
   UINT                      Count
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppResources* 
</dt> <dd>

Tipo: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***

Puntero a un [**puntero ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) que se establecerá en la matriz UAV al devolverse.

</dd> <dt>

*Offset* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Índice de la primera interfaz.

</dd> <dt>

*Recuento* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Número de elementos de la matriz.

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

[ID3DX11EffectUnorderedAccessViewVariable](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

