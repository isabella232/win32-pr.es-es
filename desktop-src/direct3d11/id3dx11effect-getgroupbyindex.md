---
title: Método ID3DX11Effect GetGroupByIndex (D3dx11effect.h)
description: Obtiene un grupo de efectos por índice.
ms.assetid: b38ecdbf-0920-48ff-a599-9629a3581d75
keywords:
- Método GetGroupByIndex Direct3D 11
- Método GetGroupByIndex Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método GetGroupByIndex
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
ms.openlocfilehash: 1dd0f629a60255ed28aa5cc426b99198867e0b23
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965032"
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

## <a name="remarks"></a>Observaciones

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

