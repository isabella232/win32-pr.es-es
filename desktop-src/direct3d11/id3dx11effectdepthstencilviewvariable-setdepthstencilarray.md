---
title: Método ID3DX11EffectDepthStencilViewVariable SetDepthStencilArray (D3dx11effect.h)
description: Establezca una matriz de recursos de vista de galería de símbolos de profundidad.
ms.assetid: 7a00ca3e-fb07-4185-a361-36228f72dcea
keywords:
- Método SetDepthStencilArray Direct3D 11
- Método SetDepthStencilArray Direct3D 11 , ID3DX11EffectDepthStencilViewVariable (interfaz)
- ID3DX11EffectDepthStencilViewVariable interface Direct3D 11 , Método SetDepthStencilArray
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.SetDepthStencilArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e6588a039d77730c42e68a977fe16e8126cf54ab502a6806a45a5190e57b26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858135"
---
# <a name="id3dx11effectdepthstencilviewvariablesetdepthstencilarray-method"></a>Id3DX11EffectDepthStencilViewVariable::SetDepthStencilArray (método)

Establezca una matriz de recursos de vista de galería de símbolos de profundidad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDepthStencilArray(
   ID3D11DepthStencilView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppResources* 
</dt> <dd>

Tipo: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***

Puntero a una matriz de interfaces de vista de galería de símbolos de profundidad. Vea [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).

</dd> <dt>

*Offset* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Índice de matriz de base cero para establecer la primera interfaz.

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
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectDepthStencilViewVariable](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

