---
title: Método ID3DX11EffectType GetMemberSemantic (D3dx11effect.h)
description: Obtiene la semántica adjunta a un miembro.
ms.assetid: e0666d4e-7510-4496-849e-a0531238b5f8
keywords:
- Método GetMemberSemantic Direct3D 11
- Método GetMemberSemantic Direct3D 11 , interfaz ID3DX11EffectType
- Interfaz ID3DX11EffectType direct3D 11, método GetMemberSemantic
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberSemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 963653f3814d0d7984966328327d1f7ece8f9a30727f361daefb91a554db1265
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069625"
---
# <a name="id3dx11effecttypegetmembersemantic-method"></a>Método ID3DX11EffectType::GetMemberSemantic

Obtiene la semántica adjunta a un miembro.

## <a name="syntax"></a>Sintaxis


```C++
LPCSTR GetMemberSemantic(
   UINT Index
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Un índice basado en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Cadena que contiene la semántica.

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

[ID3DX11EffectType](id3dx11effecttype.md)
</dt> </dl>

 

