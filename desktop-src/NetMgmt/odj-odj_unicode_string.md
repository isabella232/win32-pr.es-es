---
title: ODJ_UNICODE_STRING
description: ODJ_UNICODE_STRING definición de IDL
ms.assetid: a7999df0-d961-4fd7-ae5e-65ad79a9c17c
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f1134d7b95cca6948932bf9d79fe976d6745448a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566933"
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

## <a name="members"></a>Members

### <a name="length"></a>Length

Debe establecerse en el número de bytes del búfer que contiene la cadena, sin incluir el terminador NULL.

### <a name="maximumlength"></a>MaximumLength

Debe establecerse en el número total de bytes del búfer, sin incluir el terminador NULL.

### <a name="buffer"></a>Buffer

Debe ser una cadena Unicode.

## <a name="see-also"></a>Vea también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)
