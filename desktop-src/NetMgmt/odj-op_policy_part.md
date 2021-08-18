---
title: OP_POLICY_PART
description: OP_POLICY_PART definición de IDL
ms.assetid: 3988b298-b21d-4476-bfa5-ac606bcbd6c8
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 8ad479c2e24d8c38e87a2100658be2afcf37d70d321e99433e3b05a3af35fa60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911485"
---
# <a name="op_policy_part-structure"></a>OP_POLICY_PART estructura

Contiene una matriz de OP_POLICY_ELEMENT_LIST estructura.

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

Contiene una matriz de OP_POLICY_ELEMENT_LIST estructura.

### <a name="extension"></a>Extensión

Reservado para uso futuro y debe contener todos los ceros.

## <a name="see-also"></a>Vea también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)

[**LISTA DE \_ ELEMENTOS DE DIRECTIVA DE \_ \_ OPERACIÓN**](odj-op_policy_element_list.md)
