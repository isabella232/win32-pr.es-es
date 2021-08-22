---
title: Método ID3DX11EffectType GetMemberTypeByName (D3dx11effect.h)
description: Obtenga un tipo de miembro por nombre.
ms.assetid: 0c5a732b-7c3a-41da-b7de-dc464eed814a
keywords:
- Método GetMemberTypeByName Direct3D 11
- Método GetMemberTypeByName Direct3D 11 , interfaz ID3DX11EffectType
- Interfaz ID3DX11EffectType Direct3D 11 , método GetMemberTypeByName
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b5988a987816ad7e5a1797d60619605228647c3dd81945b63bac9c74701bf77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460715"
---
# <a name="id3dx11effecttypegetmembertypebyname-method"></a>Método ID3DX11EffectType::GetMemberTypeByName

Obtenga un tipo de miembro por nombre.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectType* GetMemberTypeByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nombre de un miembro.

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

 

