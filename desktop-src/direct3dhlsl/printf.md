---
title: printf (función)
description: Envía un mensaje de sombreador personalizado a la cola de información.
ms.assetid: 0c6c15fc-1da5-4a26-ade0-5a0489e4f564
keywords:
- función printf de HLSL
topic_type:
- apiref
api_name:
- printf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74492cc613e22f335eace684300f0380e5751a95
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994766"
---
# <a name="printf-function"></a>printf (función)

Envía un mensaje de sombreador personalizado a la cola de información.

## <a name="syntax"></a>Sintaxis

``` syntax
void printf(
   string format,
    argument ...
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*format* 
</dt> <dd>

Cadena de formato.

</dd> <dt>

*argumento...* 
</dt> <dd>

Argumentos opcionales.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta operación no hace nada en los dispositivos que no lo admiten.

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                        | Compatible |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4 (DirectX HLSL) o posterior.](dx-graphics-hlsl-sm3.md) | sí       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




