---
title: ODJ_PROVISION_DATA
description: Definición de ODJ_PROVISION_DATA IDL
ms.assetid: ff623d04-ad3f-4846-b9de-aaa280713018
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f07d8c200103fa21afc080c60157645fe6730766
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "105720196"
---
# <a name="odj_provision_data-structure"></a>Estructura de ODJ_PROVISION_DATA

Especifica la estructura de serialización más externa utilizada por las API de unión a dominio sin conexión.

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

Apunta a una matriz de estructuras de ODJ_BLOB.

## <a name="see-also"></a>Vea también

[**Definiciones IDL de unión a dominio sin conexión**](odj-idl.md)

[**\_BLOB ODJ**](odj-odj_blob.md)


