---
title: OP_JOINPROV3_PART
description: OP_JOINPROV3_PART definición de IDL
ms.assetid: 1d8bbfcf-c08e-4bc8-b569-0496703f2d67
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 81c8f53f55a8d5a284f969cbde539b0c34406903
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566905"
---
# <a name="op_joinprov3_part-structure"></a>OP_JOINPROV3_PART estructura

Contiene información adicional utilizada para configurar un cliente unido a un dominio.

## <a name="syntax"></a>Sintaxis

```C++
typedef struct _OP_JOINPROV3_PART
{
    DWORD Rid;
    [string] wchar_t *lpSid;
} OP_JOINPROV3_PART, *POP_JOINPROV3_PART;
```

## <a name="members"></a>Members

### <a name="rid"></a>Librar

Debe establecerse en el identificador relativo del SID de la cuenta de equipo.

### <a name="lpsid"></a>lpSid

Debe establecerse en el SID de la cuenta de equipo en forma de cadena.

## <a name="see-also"></a>Vea también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)
