---
title: Método ID3DX11EffectType GetMemberSemantic (D3dx11effect. h)
description: Obtiene la semántica asociada a un miembro.
ms.assetid: e0666d4e-7510-4496-849e-a0531238b5f8
keywords:
- Método GetMemberSemantic Direct3D 11
- Método GetMemberSemantic Direct3D 11, interfaz ID3DX11EffectType
- Interfaz ID3DX11EffectType Direct3D 11, método GetMemberSemantic
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
ms.openlocfilehash: 6255860dc9f7dc5cf12742e6f40b7e5148a3f27c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998383"
---
# <a name="id3dx11effecttypegetmembersemantic-method"></a>ID3DX11EffectType:: GetMemberSemantic (método)

Obtiene la semántica asociada a un miembro.

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

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Un índice basado en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Cadena que contiene la semántica.

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

[ID3DX11EffectType](id3dx11effecttype.md)
</dt> </dl>

 

