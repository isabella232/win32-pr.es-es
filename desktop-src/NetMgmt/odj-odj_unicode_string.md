---
title: ODJ_UNICODE_STRING
description: ODJ_UNICODE_STRING definición de IDL
ms.assetid: a7999df0-d961-4fd7-ae5e-65ad79a9c17c
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 3578c62f110eafd053ed97bbe1f8b5015156d02c4b879ff8111ff13f28dfab33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891245"
---
# <a name="odj_unicode_string-structure"></a>ODJ_UNICODE_STRING estructura

Contiene una cadena Unicode.

## <a name="syntax"></a>Sintaxis

```C++
typedef struct _ODJ_UNICODE_STRING
{
    USHORT Length;
    USHORT MaximumLength;
    [size_is(MaximumLength/2), length_is(Length/2)] PWSTR Buffer;
} ODJ_UNICODE_STRING, *PODJ_UNICODE_STRING;
```

## <a name="members"></a>Miembros

### <a name="length"></a>Length

Debe establecerse en el número de bytes del búfer que contiene la cadena, sin incluir el terminador NULL.

### <a name="maximumlength"></a>MaximumLength

Debe establecerse en el número total de bytes del búfer, sin incluir el terminador NULL.

### <a name="buffer"></a>Buffer

Debe ser una cadena Unicode.

## <a name="see-also"></a>Vea también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)
