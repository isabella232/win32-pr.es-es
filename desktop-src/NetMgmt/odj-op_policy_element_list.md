---
title: OP_POLICY_ELEMENT_LIST
description: Definición de OP_POLICY_ELEMENT_LIST IDL
ms.assetid: 1eebbdd2-655b-4bd3-938c-6bc687ffe7bb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 3c46e7208e6c142b9f58a7704be9bd3461c845b2
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "103797175"
---
# <a name="op_policy_element_list-structure"></a>Estructura de OP_POLICY_ELEMENT_LIST

Define una clave del Registro raíz y una matriz de elementos de clave del registro que se van a configurar bajo esa clave.

## <a name="syntax"></a>Sintaxis

```C++
typedef struct _OP_POLICY_ELEMENT_LIST
{
    [string] wchar_t                            *pSource;
    ULONG                                       ulRootKeyId;
    ULONG                                       cElements;
    [size_is(cElements)]    POP_POLICY_ELEMENT  pElements;
} OP_POLICY_ELEMENT_LIST, *POP_POLICY_ELEMENT_LIST;
```

## <a name="members"></a>Miembros

### <a name="psource"></a>pSource

Contiene la ruta de acceso del archivo directiva de grupo desde el que se produjeron los elementos contenidos.

### <a name="ulrootkeyid"></a>ulRootKeyId

Contiene el identificador de la clave del Registro raíz; Actualmente debe establecerse en HKEY_LOCAL_MACHINE.

### <a name="celements"></a>cElements

Contiene el número de elementos de los mismos.

### <a name="pelements"></a>Los mismos

Contiene una matriz de elementos OP_POLICY_ELEMENT.

## <a name="see-also"></a>Vea también

[**Definiciones IDL de unión a dominio sin conexión**](odj-idl.md)

[**\_elemento de directiva de OP \_**](odj-op_policy_element.md)
