---
title: Método ID3DX11EffectRasterizerVariable UndoSetRasterizerState (D3dx11effect.h)
description: Revierte un estado de rasterizador establecido previamente.
ms.assetid: 2801479c-cb70-4950-9888-73e271b669aa
keywords:
- Método UndoSetRasterizerState Direct3D 11
- Método UndoSetRasterizerState Direct3D 11 , interfaz ID3DX11EffectRasterizerVariable
- Id3DX11EffectRasterizerVariable interface Direct3D 11 , UndoSetRasterizerState method
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.UndoSetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3c49f46b357108cb53959bc9b6e3b6d71d62979629da0f44606bec978a855ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045863"
---
# <a name="id3dx11effectrasterizervariableundosetrasterizerstate-method"></a>Método ID3DX11EffectRasterizerVariable::UndoSetRasterizerState

Revierte un estado de rasterizador establecido previamente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UndoSetRasterizerState(
   UINT Index
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indexe en una matriz de interfaces de rasterizador. Si solo hay una interfaz de rasterizador, use 0.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectRasterizerVariable](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

