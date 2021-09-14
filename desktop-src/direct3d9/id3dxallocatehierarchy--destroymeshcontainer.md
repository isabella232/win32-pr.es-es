---
description: Solicita la desasignación de un objeto de contenedor de malla.
ms.assetid: 7a976ba8-6972-4857-b0a9-4ea7a88dc8ac
title: Método ID3DXAllocateHierarchy::D estroyMeshContainer (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.DestroyMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6114c78cefd7415fb11fc30587fa2dc628fb4466
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969683"
---
# <a name="id3dxallocatehierarchydestroymeshcontainer-method"></a>Método ID3DXAllocateHierarchy::D estroyMeshContainer

Solicita la desasignación de un objeto de contenedor de malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DestroyMeshContainer(
  [in] LPD3DXMESHCONTAINER pMeshContainerToFree
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMeshContainerToFree* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**

Puntero al objeto de contenedor de malla que se va a desasignar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Los valores devueltos de este método los implementa un programador de aplicaciones. En general, si no se produce ningún error, programe el método para devolver D3D \_ OK. De lo contrario, programe el método para devolver un mensaje de error adecuado de D3DERR o D3DXERR, ya que esto hará que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) también devuelva el error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXAllocateHierarchy](id3dxallocatehierarchy.md)
</dt> </dl>

 

 




