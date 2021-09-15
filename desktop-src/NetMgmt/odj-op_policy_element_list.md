---
title: OP_POLICY_ELEMENT_LIST
description: OP_POLICY_ELEMENT_LIST definición de IDL
ms.assetid: 1eebbdd2-655b-4bd3-938c-6bc687ffe7bb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 3c46e7208e6c142b9f58a7704be9bd3461c845b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566889"
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

## <a name="members"></a>Members

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
