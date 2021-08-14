---
description: Obtiene el período del conjunto de animación.
ms.assetid: 0bb19ec1-c918-44b6-83b0-4fdbb4e1a485
title: Método ID3DXAnimationSet::GetPeriod (D3dx9anim.h)
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
ms.openlocfilehash: d8e984d1593fbbd79561bbb15fb27b62a9961c1830c42465ed529f08c374e180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118522334"
---
# <a name="id3dxanimationsetgetperiod-method"></a>Método ID3DXAnimationSet::GetPeriod

Obtiene el período del conjunto de animación.

## <a name="syntax"></a>Sintaxis


```C++
DOUBLE GetPeriod();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Punto del conjunto de animación.

## <a name="remarks"></a>Comentarios

El período es el intervalo de tiempo durante el que los fotogramas clave de animación son válidos. Para las animaciones de bucle, este es el período del bucle. La aplicación determina las unidades de tiempo en las que se especifican los fotogramas clave (por ejemplo, segundos).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
