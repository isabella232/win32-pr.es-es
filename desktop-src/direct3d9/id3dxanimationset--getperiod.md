---
description: Obtiene el período del conjunto de animaciones.
ms.assetid: 0bb19ec1-c918-44b6-83b0-4fdbb4e1a485
title: 'ID3DXAnimationSet:: GetPeriod (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriod
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f6eafbfe802afc8ff3084c49acf31addca66cef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698419"
---
# <a name="id3dxanimationsetgetperiod-method"></a>ID3DXAnimationSet:: GetPeriod (método)

Obtiene el período del conjunto de animaciones.

## <a name="syntax"></a>Sintaxis


```C++
DOUBLE GetPeriod();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Período del conjunto de animaciones.

## <a name="remarks"></a>Observaciones

El período es el intervalo de tiempo en el que los fotogramas clave de la animación son válidos. En el caso de las animaciones de bucle, este es el período del bucle. La aplicación determina las unidades de tiempo en las que se especifican los fotogramas clave (por ejemplo, segundos).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
