---
description: Busca el marco secundario de un marco raíz.
ms.assetid: 211e117a-9707-459a-a6a1-b3e78bdad6e2
title: Función D3DXFrameFind (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameFind
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 82b8c56c93f19c99441b93707fac2a0c150e0c38
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567929"
---
# <a name="d3dxframefind-function"></a>Función D3DXFrameFind

Busca el marco secundario de un marco raíz.

## <a name="syntax"></a>Sintaxis


```C++
LPD3DXFRAME D3DXFrameFind(
  _In_ const D3DXFRAME *pFrameRoot,
  _In_       LPCSTR    Name
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFrameRoot* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***

Puntero al marco raíz. Vea [**D3DXFRAME.**](d3dxframe.md)

</dd> <dt>

*Nombre* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nombre del marco secundario que se buscará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**

Devuelve el marco secundario si se encuentra o **NULL** en caso contrario. Vea [**D3DXFRAME.**](d3dxframe.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de animación](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
