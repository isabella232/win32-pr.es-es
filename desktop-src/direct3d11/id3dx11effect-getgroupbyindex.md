---
title: Método ID3DX11Effect GetGroupByIndex (D3dx11effect. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003921"
---
# <a name="id3dx11effectgetgroupbyindex-method"></a>ID3DX11Effect:: GetGroupByIndex (método)

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

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Índice del grupo de efectos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***

Puntero a una interfaz [**ID3DX11EffectGroup**](id3dx11effectgroup.md) .

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

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

