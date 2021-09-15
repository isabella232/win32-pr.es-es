---
description: Devuelve el nivel de controlador.
ms.assetid: e8c85201-7850-4c8d-a124-ceb76d4e24d5
title: Función D3DXGetDriverLevel (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDriverLevel
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 83f756f6b6ab5864f14e797879be243f871fb9e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567897"
---
# <a name="d3dxgetdriverlevel-function"></a>Función D3DXGetDriverLevel

Devuelve el nivel de controlador.

## <a name="syntax"></a>Sintaxis


```C++
UINT D3DXGetDriverLevel(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una [**interfaz IDirect3DDevice9 que**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) representa el dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Nivel de controlador. Vea Notas.

## <a name="remarks"></a>Observaciones

Este método devuelve la versión del controlador, que es una de las siguientes:

-   700: controlador de nivel 7 de Direct3D
-   800: controlador de nivel 8 de Direct3D
-   900: controlador de nivel 9 de Direct3D

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[De uso general Functions](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
