---
title: Función CheckAccessFullyMapped
description: Determina si todos los valores de una operación Sample, Gather o Load accedieron a iconos asignados en un recurso en mosaico.
ms.assetid: 2CAB7770-143E-4E29-A57F-96C27021AC5F
keywords:
- Función CheckAccessFullyMapped HLSL
topic_type:
- apiref
api_name:
- CheckAccessFullyMapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e7241fa5546edffb2b7c5ff36d2e43919e6d0b6fef9ff617c0fb63a674ffee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516678"
---
# <a name="checkaccessfullymapped-function"></a>Función CheckAccessFullyMapped

Determina si todos los valores de una operación **Sample**, **Gather** o **Load** accedieron a iconos asignados en un recurso [en mosaico.](/windows/desktop/direct3d11/direct3d-11-2-features)

## <a name="syntax"></a>Sintaxis

``` syntax
bool CheckAccessFullyMapped(
  in uint_only status
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*status* \[ En\]
</dt> <dd>

Tipo: **solo \_ uint**

Valor de estado que se devuelve de una **operación Sample**, **Gather** **o Load.** Dado que no puede acceder directamente a este valor de estado, debe pasarlo a **CheckAccessFullyMapped**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **bool**

Devuelve un **valor booleano** que indica si todos los valores de una operación **Sample**, **Gather** o **Load** accedieron a iconos asignados en un recurso [en mosaico.](/windows/desktop/direct3d11/direct3d-11-2-features) Devuelve **TRUE si** todos los valores de la operación accedieron a iconos asignados; de lo contrario, **devuelve FALSE** si se han tomado valores de un icono no atado.

## <a name="remarks"></a>Comentarios

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | Sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 