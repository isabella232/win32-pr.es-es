---
title: ODJ_UNICODE_STRING
description: Definición de ODJ_UNICODE_STRING IDL
ms.assetid: a7999df0-d961-4fd7-ae5e-65ad79a9c17c
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f1134d7b95cca6948932bf9d79fe976d6745448a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "105720193"
---
# <a name="odj_unicode_string-structure"></a>Estructura de ODJ_UNICODE_STRING

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

Debe establecerse en el número de bytes en el búfer que contiene la cadena, sin incluir el terminador NULL.

### <a name="maximumlength"></a>MaximumLength

DEBE establecerse en el número total de bytes en el búfer, sin incluir el terminador NULL.

### <a name="buffer"></a>Buffer

Debe ser una cadena Unicode.

## <a name="see-also"></a>Vea también

[**Definiciones IDL de unión a dominio sin conexión**](odj-idl.md)
