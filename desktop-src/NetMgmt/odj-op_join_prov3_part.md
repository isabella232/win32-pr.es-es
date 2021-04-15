---
title: OP_JOINPROV3_PART
description: Definición de OP_JOINPROV3_PART IDL
ms.assetid: 1d8bbfcf-c08e-4bc8-b569-0496703f2d67
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 81c8f53f55a8d5a284f969cbde539b0c34406903
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "104421566"
---
# <a name="op_joinprov3_part-structure"></a>Estructura de OP_JOINPROV3_PART

Contiene información adicional que se usa para configurar un cliente unido a un dominio.

## <a name="syntax"></a>Sintaxis

```C++
typedef struct _OP_JOINPROV3_PART
{
    DWORD Rid;
    [string] wchar_t *lpSid;
} OP_JOINPROV3_PART, *POP_JOINPROV3_PART;
```

## <a name="members"></a>Miembros

### <a name="rid"></a>Libra

Debe establecerse en el identificador relativo del SID de la cuenta de la máquina.

### <a name="lpsid"></a>lpSid

Debe establecerse en el SID de la cuenta de la máquina en forma de cadena.

## <a name="see-also"></a>Vea también

[**Definiciones IDL de unión a dominio sin conexión**](odj-idl.md)
