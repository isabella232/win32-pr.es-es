---
title: OP_POLICY_ELEMENT
description: Definición de OP_POLICY_ELEMENT IDL
ms.assetid: 69f6e0e7-3f47-4fee-8a4c-df94093dcffa
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: df6fc6852a5efd0a6a2e01a805878ed51bc7c263
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "104359564"
---
# <a name="op_policy_element-structure"></a>Estructura de OP_POLICY_ELEMENT

Define una clave del registro y un nombre de valor, tipo y valor que deben configurarse bajo esa clave.

## <a name="syntax"></a>Sintaxis

```C++
typedef struct _OP_POLICY_ELEMENT
{
    [string] wchar_t                *pKeyPath;
    [string] wchar_t                *pValueName;
    ULONG                           ulValueType;
    ULONG                           cbValueData;
    [size_is(cbValueData)]  PBYTE   pValueData;
} OP_POLICY_ELEMENT, *POP_POLICY_ELEMENT;
```

## <a name="members"></a>Miembros

### <a name="pkeypath"></a>pKeyPath

Contiene la ruta de acceso de la clave del registro.

### <a name="pvaluename"></a>pValueName

Contiene el nombre del valor del registro.

### <a name="ulvaluetype"></a>ulValueType

Contiene uno de los valores de los [tipos de valor del registro](../sysinfo/registry-value-types.md).

### <a name="cbvaluedata"></a>cbValueData

Contiene el tamaño de pValueData en bytes.

### <a name="ulvaluetype"></a>ulValueType

Contiene el valor del valor del registro.

## <a name="see-also"></a>Vea también

[**Definiciones IDL de unión a dominio sin conexión**](odj-idl.md)