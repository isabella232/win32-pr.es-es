---
description: Cargar datos secundarios de la malla desde un archivo. x.
ms.assetid: 5ed338f9-48a6-44e6-95da-1bed9ecd6ebf
title: 'ID3DXLoadUserData:: LoadMeshChildData (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9960f47ac21dad2521f6272c9176e3d895bbd109
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717656"
---
# <a name="id3dxloaduserdataloadmeshchilddata-method"></a>ID3DXLoadUserData:: LoadMeshChildData (método)

Cargar datos secundarios de la malla desde un archivo. x.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LoadMeshChildData(
  [in] LPD3DXMESHCONTAINER pMeshContainer,
  [in] LPD3DXFILEDATA      pXofChildData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMeshContainer* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**

Puntero a un contenedor de malla. Vea [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).

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

 

 




