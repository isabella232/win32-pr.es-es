---
description: Cargar datos secundarios de marco desde un archivo. x.
ms.assetid: 79d251f3-c661-42e3-9385-84aabd58fd4f
title: 'ID3DXLoadUserData:: LoadFrameChildData (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 53bde98f0e756fd1baff4c509179f15e8489e74f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548102"
---
# <a name="id3dxloaduserdataloadframechilddata-method"></a>ID3DXLoadUserData:: LoadFrameChildData (método)

Cargar datos secundarios de marco desde un archivo. x.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LoadFrameChildData(
  [in] LPD3DXFRAME    pFrame,
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFrame* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**

Puntero a un contenedor de malla. Vea [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*pXofChildData* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**

Puntero a una estructura de datos de archivo. x. Esto se define en Dxfile. h.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Un programador de aplicaciones implementa los valores devueltos de este método. En general, si no se produce ningún error, programe el método para devolver D3D \_ OK. De lo contrario, programe el método para que devuelva un mensaje de error adecuado de D3DERR o D3DXERR, ya que esto hará que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) también produzca un error y devuelva el error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXLoadUserData](id3dxloaduserdata.md)
</dt> </dl>

 

 




