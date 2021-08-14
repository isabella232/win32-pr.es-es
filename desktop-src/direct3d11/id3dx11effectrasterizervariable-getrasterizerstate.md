---
title: Método ID3DX11EffectRasterizerVariable GetRasterizerState (D3dx11effect.h)
description: Obtiene un puntero a una interfaz rasterizadora.
ms.assetid: 4b8515e0-b79a-4572-9142-07c50a8839b8
keywords:
- Método GetRasterizerState Direct3D 11
- Método GetRasterizerState Direct3D 11 , interfaz ID3DX11EffectRasterizerVariable
- Interfaz ID3DX11EffectRasterizerVariable Direct3D 11, método GetRasterizerState
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94dbd6b45b14e8499fada4c1c5eb32b9bbd55b1dad843b05cf52a9318737cb9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045883"
---
# <a name="id3dx11effectrasterizervariablegetrasterizerstate-method"></a>Método ID3DX11EffectRasterizerVariable::GetRasterizerState

Obtiene un puntero a una interfaz rasterizadora.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRasterizerState(
   UINT                  Index,
   ID3D11RasterizerState **ppRasterizerState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indexe en una matriz de interfaces de rasterizador. Si solo hay una interfaz de rasterizador, use 0.

</dd> <dt>

*ppRasterizerState* 
</dt> <dd>

Tipo: **[ **ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\*\***

Dirección de un puntero a una interfaz de rasterizador (vea [**ID3D11RasterizerState).**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Observaciones

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectRasterizerVariable](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

