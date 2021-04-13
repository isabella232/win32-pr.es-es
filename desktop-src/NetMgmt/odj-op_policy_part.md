---
title: OP_POLICY_PART
description: Definición de OP_POLICY_PART IDL
ms.assetid: 3988b298-b21d-4476-bfa5-ac606bcbd6c8
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: ef0e3b96ce564ed7ff8e2ce0886e33ca474a1cf8
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "104421569"
---
# <a name="op_policy_part-structure"></a>Estructura de OP_POLICY_PART

Contiene una matriz de estructuras OP_POLICY_ELEMENT_LIST.

## <a name="syntax"></a>Sintaxis

```C++
typedef struct _OP_POLICY_PART
{
    ULONG                                       cElementLists;
    [size_is(cElementLists)]
                        POP_POLICY_ELEMENT_LIST pElementLists;
    OP_BLOB                                     Extension;
} OP_POLICY_PART, *POP_POLICY_PART;
```

## <a name="members"></a>Miembros

### <a name="celementlists"></a>cElementLists

Contiene el número de elementos de pElementLists.

### <a name="pelementlists"></a>pElementLists

Contiene una matriz de estructuras OP_POLICY_ELEMENT_LIST.

### <a name="extension"></a>Extensión

Reservado para uso futuro y debe contener ceros.

## <a name="see-also"></a>Vea también

[**Definiciones IDL de unión a dominio sin conexión**](odj-idl.md)

[**\_lista de \_ elementos de directiva de OP \_**](odj-op_policy_element_list.md)
