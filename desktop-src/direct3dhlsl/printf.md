---
title: printf (función)
description: Envía un mensaje de sombreador personalizado a la cola de información.
ms.assetid: 0c6c15fc-1da5-4a26-ade0-5a0489e4f564
keywords:
- función printf HLSL
topic_type:
- apiref
api_name:
- printf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47131cacef436572f519b394a02b4aaa357a426dd80a192868712cb3d7779e24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672525"
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

 

 




