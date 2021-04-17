---
description: Solicita la asignación de un objeto de contenedor de malla.
ms.assetid: ec66b393-016b-4572-94dc-5c8903b506a3
title: 'ID3DXAllocateHierarchy:: CreateMeshContainer (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.CreateMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0351290b8dee260d52362702d520b01e1bcb7af3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698180"
---
# <a name="id3dxallocatehierarchycreatemeshcontainer-method"></a>ID3DXAllocateHierarchy:: CreateMeshContainer (método)

Solicita la asignación de un objeto de contenedor de malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateMeshContainer(
  [in]                LPCSTR              Name,
  [in]          const D3DXMESHDATA        *pMeshData,
  [in]          const D3DXMATERIAL        *pMaterials,
  [in]          const D3DXEFFECTINSTANCE  *pEffectInstances,
  [in]                DWORD               NumMaterials,
  [in]          const DWORD               *pAdjacency,
  [in]                LPD3DXSKININFO      pSkinInfo,
  [out, retval]       LPD3DXMESHCONTAINER *ppNewMeshContainer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* \[ de de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nombre de la malla.

</dd> <dt>

*pMeshData* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMESHDATA**](d3dxmeshdata.md) \***

Puntero a la estructura de datos de malla. Vea [**D3DXMESHDATA**](d3dxmeshdata.md).

</dd> <dt>

*pMaterials* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATERIAL**](d3dxmaterial.md) \***

Matriz de materiales utilizados en la malla.

</dd> <dt>

*pEffectInstances* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***

Matriz de instancias de efecto usadas en la malla. Vea [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).

</dd> <dt>

*NumMaterials* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de materiales en la matriz de materiales.

</dd> <dt>

*pAdjacency* \[ de\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Matriz de adyacencias para la malla.

</dd> <dt>

*pSkinInfo* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)**

Puntero al objeto de malla de máscara si se encuentran datos de máscara. Vea [**ID3DXSkinInfo**](id3dxskininfo.md).

</dd> <dt>

*ppNewMeshContainer* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***

Devuelve el contenedor de malla creado. Vea [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).

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

[ID3DXAllocateHierarchy](id3dxallocatehierarchy.md)
</dt> </dl>

 

 
