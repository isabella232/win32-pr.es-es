---
title: OP_POLICY_ELEMENT
description: OP_POLICY_ELEMENT definición de IDL
ms.assetid: 69f6e0e7-3f47-4fee-8a4c-df94093dcffa
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 74e81f09f4d45d42f5e9df585b88051ac1e96e8cd33e4c15807701e61825b43b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983389"
---
# <a name="op_policy_element-structure"></a>OP_POLICY_ELEMENT estructura

Define una clave del Registro y un nombre, tipo y valor de valor que se deben configurar en esa clave.

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

Contiene la ruta de acceso de la clave del Registro.

### <a name="pvaluename"></a>pValueName

Contiene el nombre del valor del Registro.

### <a name="ulvaluetype"></a>ulValueType

Contiene uno de los valores de Tipos [de valor del Registro.](../sysinfo/registry-value-types.md)

### <a name="cbvaluedata"></a>cbValueData

Contiene el tamaño de pValueData en bytes.

### <a name="ulvaluetype"></a>ulValueType

Contiene el valor del registro.

## <a name="see-also"></a>Vea también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)