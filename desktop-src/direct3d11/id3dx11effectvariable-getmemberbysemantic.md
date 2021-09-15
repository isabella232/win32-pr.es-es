---
title: Método ID3DX11EffectVariable GetMemberBySemantic (D3dx11effect.h)
description: Obtener un miembro de estructura por semántica.
ms.assetid: e4ae1f6a-43d2-45df-9dba-833d4f767818
keywords:
- Método GetMemberBySemantic Direct3D 11
- Método GetMemberBySemantic Direct3D 11 , interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable direct3D 11 , método GetMemberBySemantic
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5af8b628247dcc89f8df99c6ffebb04d500e76a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569993"
---
# <a name="id3dx11effectvariablegetmemberbysemantic-method"></a>Método ID3DX11EffectVariable::GetMemberBySemantic

Obtener un miembro de estructura por semántica.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectVariable* GetMemberBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Semántica* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Semántica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Puntero a [**id3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Observaciones

Si la variable de efecto es una estructura, use este método para buscar un miembro mediante la semántica adjunta.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

