---
description: Cargar datos secundarios de marco desde un archivo .x.
ms.assetid: 79d251f3-c661-42e3-9385-84aabd58fd4f
title: Método ID3DXLoadUserData::LoadFrameChildData (D3dx9anim.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568953"
---
# <a name="id3dxloaduserdataloadframechilddata-method"></a>Método ID3DXLoadUserData::LoadFrameChildData

Cargar datos secundarios de marco desde un archivo .x.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LoadFrameChildData(
  [in] LPD3DXFRAME    pFrame,
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFrame* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**

Puntero a un contenedor de malla. Vea [**D3DXFRAME.**](d3dxframe.md)

</dd> <dt>

*pXofChildData* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**

Puntero a una estructura de datos de archivo .x. Esto se define en Dxfile.h.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Los valores devueltos de este método los implementa un programador de aplicaciones. En general, si no se produce ningún error, programe el método para devolver D3D \_ OK. De lo contrario, programe el método para devolver un mensaje de error adecuado de D3DERR o D3DXERR, ya que esto hará que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) también presente un error y devuelva el error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXLoadUserData](id3dxloaduserdata.md)
</dt> </dl>

 

 




