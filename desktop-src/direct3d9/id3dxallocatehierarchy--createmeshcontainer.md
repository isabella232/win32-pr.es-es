---
description: Solicita la asignación de un objeto de contenedor de malla.
ms.assetid: ec66b393-016b-4572-94dc-5c8903b506a3
title: Método ID3DXAllocateHierarchy::CreateMeshContainer (D3dx9anim.h)
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
ms.openlocfilehash: fee8b9222358f343b6a8e23435815c8c484a6c8ce86625303e127174d300a197
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026875"
---
# <a name="id3dxallocatehierarchycreatemeshcontainer-method"></a>Método ID3DXAllocateHierarchy::CreateMeshContainer

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

*Nombre* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nombre de la malla.

</dd> <dt>

*pMeshData* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMESHDATA**](d3dxmeshdata.md) \***

Puntero a la estructura de datos de malla. Vea [**D3DXMESHDATA.**](d3dxmeshdata.md)

</dd> <dt>

*pMaterials* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATERIAL**](d3dxmaterial.md) \***

Matriz de materiales usados en la malla.

</dd> <dt>

*pEffectInstances* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***

Matriz de instancias de efecto usadas en la malla. Vea [**D3DXEFFECTINSTANCE.**](d3dxeffectinstance.md)

</dd> <dt>

*NumMaterials* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de materiales de la matriz de materiales.

</dd> <dt>

*pAdjacency* \[ En\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Matriz de adyacencias para la malla.

</dd> <dt>

*pSkinInfo* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)**

Puntero al objeto de malla de máscara si se encuentran datos de máscara. Vea [**ID3DXSkinInfo.**](id3dxskininfo.md)

</dd> <dt>

*ppNewMeshContainer* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***

Devuelve el contenedor de malla creado. Vea [**D3DXMESHCONTAINER.**](d3dxmeshcontainer.md)

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

[ID3DXAllocateHierarchy](id3dxallocatehierarchy.md)
</dt> </dl>

 

 
