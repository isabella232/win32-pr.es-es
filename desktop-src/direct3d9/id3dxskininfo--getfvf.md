---
description: Obtiene el valor de vértice de función fijo.
ms.assetid: 9b80c4b9-2e5b-4965-99b9-ad6c459ef413
title: 'ID3DXSkinInfo:: GetFVF (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6d48cd9cea6efd6cb43e6da6877a7aaf42909c71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362413"
---
# <a name="id3dxskininfogetfvf-method"></a>ID3DXSkinInfo:: GetFVF (método)

Obtiene el valor de vértice de función fijo.

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetFVF();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Devuelve los códigos de formato de vértice flexible (FVF).

## <a name="remarks"></a>Observaciones

Este método puede devolver 0 si el formato de vértice no se puede asignar directamente a un código FVF. Esto ocurrirá en una malla creada a partir de una declaración de vértices que no tiene el mismo orden y los mismos elementos que los códigos de FVF.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetFVF**](id3dxskininfo--setfvf.md)
</dt> </dl>

 

 
