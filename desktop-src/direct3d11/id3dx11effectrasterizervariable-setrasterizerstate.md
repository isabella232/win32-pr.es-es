---
title: Método ID3DX11EffectRasterizerVariable SetRasterizerState (D3dx11effect. h)
description: Establece el estado del rasterizador.
ms.assetid: b2cd93fb-77bb-4a39-b686-7b8f683c9172
keywords:
- Método SetRasterizerState Direct3D 11
- Método SetRasterizerState Direct3D 11, interfaz ID3DX11EffectRasterizerVariable
- Interfaz ID3DX11EffectRasterizerVariable Direct3D 11, método SetRasterizerState
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.SetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c1f44df653339f274207bfa4283fc8470c8844f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280522"
---
# <a name="id3dx11effectrasterizervariablesetrasterizerstate-method"></a>ID3DX11EffectRasterizerVariable:: SetRasterizerState (método)

Establece el estado del rasterizador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetRasterizerState(
   UINT                  Index,
   ID3D11RasterizerState *pRasterizerState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Índice en una matriz de interfaces de rasterizador. Si solo hay una interfaz de rasterización, use 0.

</dd> <dt>

*pRasterizerState* 
</dt> <dd>

Tipo: **[ **ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\***

Puntero a una interfaz [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate) .

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

[ID3DX11EffectRasterizerVariable](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

