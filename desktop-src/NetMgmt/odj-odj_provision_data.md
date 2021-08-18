---
title: ODJ_PROVISION_DATA
description: ODJ_PROVISION_DATA definición de IDL
ms.assetid: ff623d04-ad3f-4846-b9de-aaa280713018
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 02762a80be9bd60b7f9c8648c9bfb848f3d76184f249567c9e9522189692e0e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064355"
---
# <a name="odj_provision_data-structure"></a>ODJ_PROVISION_DATA estructura

Especifica la estructura de serialización más externa utilizada por las API de combinación de dominio sin conexión.

## <a name="syntax"></a>Sintaxis

```C++
typedef struct _ODJ_PROVISION_DATA
{
    ULONG ulVersion;
    ULONG ulcBlobs;
    [size_is(ulcBlobs)] PODJ_BLOB pBlobs;
} ODJ_PROVISION_DATA;
```

## <a name="members"></a>Miembros

### <a name="ulversion"></a>ulVersion

Debe establecerse en 1.

### <a name="ulcblobs"></a>ulcBlobs

Debe establecerse en el número de elementos de la matriz pBlobs.

### <a name="pblobs"></a>pBlobs

Apunta a una matriz de ODJ_BLOB estructura.

## <a name="see-also"></a>Consulte también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)

[**BLOB \_ DE ODJ**](odj-odj_blob.md)


