---
title: Método ID3DX11Effect GetGroupByIndex (D3dx11effect.h)
description: Obtiene un grupo de efectos por índice.
ms.assetid: b38ecdbf-0920-48ff-a599-9629a3581d75
keywords:
- Método GetGroupByIndex Direct3D 11
- Método GetGroupByIndex Direct3D 11 , interfaz ID3DX11Effect
- ID3DX11Effect interface Direct3D 11 , GetGroupByIndex method
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184971eea69f80f105aa29bb3dac9decbeb18d3452ca29656a150d4f1e5d9e08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632475"
---
# <a name="id3dx11effectgetgroupbyindex-method"></a>Método ID3DX11Effect::GetGroupByIndex

Obtiene un grupo de efectos por índice.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectGroup* GetGroupByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Índice del grupo de efectos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***

Puntero a una [**interfaz ID3DX11EffectGroup.**](id3dx11effectgroup.md)

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

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

