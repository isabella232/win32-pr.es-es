---
title: errorf función)
description: Envía un mensaje de error a la cola de información.
ms.assetid: bf4dc6dc-b36e-4b71-ad61-b7a5ba332879
keywords:
- errorf de función HLSL
topic_type:
- apiref
api_name:
- errorf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76c8fbcd9b6cb15dbbb735296a3aada8f5e568cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076610"
---
# <a name="errorf-function"></a>errorf función)

Envía un mensaje de error a la cola de información.

## <a name="syntax"></a>Sintaxis

``` syntax
void errorf(
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

 

 




