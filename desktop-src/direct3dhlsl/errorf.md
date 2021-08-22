---
title: función errorf
description: Envía un mensaje de error a la cola de información.
ms.assetid: bf4dc6dc-b36e-4b71-ad61-b7a5ba332879
keywords:
- función de errorf HLSL
topic_type:
- apiref
api_name:
- errorf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0651a27419a369721806e9aa4717a20088f8f5fbbaa0063628d2feb69648c7cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562685"
---
# <a name="errorf-function"></a>función errorf

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

*Argumento...* 
</dt> <dd>

Argumentos opcionales.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta operación no hace nada en los dispositivos que no la admiten.

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                        | Compatible |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4 (DirectX HLSL) o posterior.](dx-graphics-hlsl-sm3.md) | Sí       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




