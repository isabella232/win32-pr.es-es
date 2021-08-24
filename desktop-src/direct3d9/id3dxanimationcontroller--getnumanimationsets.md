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
ms.openlocfilehash: 07a6eee85c515c4b8e923aa9973eddc648ef95cbc152c27951154a7c41fbcf3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026825"
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

Número de conjuntos de animación.

## <a name="remarks"></a>Comentarios

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

 

 
