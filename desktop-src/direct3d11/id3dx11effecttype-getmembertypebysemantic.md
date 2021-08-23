---
title: Método ID3DX11EffectType GetMemberTypeBySemantic (D3dx11effect.h)
description: Obtiene un tipo de miembro por semántica.
ms.assetid: d5fea2d9-8d08-4e02-a9c6-dbcfaaf4a7d1
keywords:
- Método GetMemberTypeBySemantic Direct3D 11
- Método GetMemberTypeBySemantic Direct3D 11 , interfaz ID3DX11EffectType
- Interfaz ID3DX11EffectType Direct3D 11 , método GetMemberTypeBySemantic
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9e1add6ddc485f803512050795b9ba240f2a29d145fb01e864b88bc8ba84ee7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532337"
---
# <a name="id3dx11effecttypegetmembertypebysemantic-method"></a>Método ID3DX11EffectType::GetMemberTypeBySemantic

Obtiene un tipo de miembro por semántica.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectType* GetMemberTypeBySemantic(
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

Tipo: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***

Puntero a [**id3DX11EffectType.**](id3dx11effecttype.md)

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

 

