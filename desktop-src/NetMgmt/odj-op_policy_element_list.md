---
title: OP_POLICY_ELEMENT_LIST
description: OP_POLICY_ELEMENT_LIST definición de IDL
ms.assetid: 1eebbdd2-655b-4bd3-938c-6bc687ffe7bb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 1fde1bb1d2794be4fd1bf799282a0257b78ae213453566208ff64bcf7a312654
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796883"
---
# <a name="op_policy_element_list-structure"></a>OP_POLICY_ELEMENT_LIST estructura

Define una clave raíz del Registro y una matriz de elementos de clave del Registro que se configurarán en esa clave.

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

Contiene la ruta de acceso del directiva de grupo del que se han origen los elementos contenidos.

### <a name="ulrootkeyid"></a>ulRootKeyId

Contiene el identificador de la clave raíz del Registro; actualmente debe establecerse en HKEY_LOCAL_MACHINE.

### <a name="celements"></a>cElements

Contiene el número de elementos de pElements.

### <a name="pelements"></a>pElements

Contiene una matriz de OP_POLICY_ELEMENT elementos.

## <a name="see-also"></a>Vea también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)

[**ELEMENTO \_ DE DIRECTIVA DE \_ OPERACIÓN**](odj-op_policy_element.md)
