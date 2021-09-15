---
description: Devuelve el número de conjuntos de animación registrados actualmente en el controlador de animación.
ms.assetid: 1aacc84d-5025-4601-9a6c-84b3d9b06012
title: Método ID3DXAnimationController::GetNumAnimationSets (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetNumAnimationSets
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5baedb0ea30d51cbd659e597cb000a434ec1632
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466075"
---
# <a name="id3dxanimationcontrollergetnumanimationsets-method"></a>Método ID3DXAnimationController::GetNumAnimationSets

Devuelve el número de conjuntos de animación registrados actualmente en el controlador de animación.

## <a name="syntax"></a>Sintaxis


```C++
UINT GetNumAnimationSets();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de conjuntos de animaciones.

## <a name="remarks"></a>Observaciones

El controlador contiene cualquier número de conjuntos de animaciones y pistas. Los conjuntos de animaciones se pueden registrar [**con RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md). Un controlador de animación creado por una llamada a [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) registrará automáticamente los conjuntos de animación cargados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
