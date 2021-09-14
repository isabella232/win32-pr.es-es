---
title: función abort (Corecrt \_ terminate.h)
description: Envía un mensaje de error a la cola de información y finaliza la llamada a draw o dispatch actual que se está ejecutando.
ms.assetid: b8ce153b-0d1c-4294-b88e-b7e50e708ab9
keywords:
- función abort HLSL
topic_type:
- apiref
api_name:
- abort
api_location:
- corecrt_terminate.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9428a03b422aed9ff6fae097459a53369d3a30e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264428"
---
# <a name="abort-function"></a>abort (función)

Envía un mensaje de error a la cola de información y finaliza la llamada a draw o dispatch actual que se está ejecutando.

## <a name="syntax"></a>Sintaxis

``` syntax
void abort(
    
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

 
</dt> <dd>

None

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta operación no hace nada en los rasterizadores que no la admiten.

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                        | Compatible |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4 (DirectX HLSL) o posterior.](dx-graphics-hlsl-sm3.md) | sí       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Corecrt \_ terminate.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





