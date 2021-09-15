---
title: ODJ_PROVISION_DATA
description: ODJ_PROVISION_DATA definición de IDL
ms.assetid: ff623d04-ad3f-4846-b9de-aaa280713018
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f07d8c200103fa21afc080c60157645fe6730766
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566944"
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

## <a name="members"></a>Members

### <a name="ulversion"></a>ulVersion

Debe establecerse en 1.

### <a name="ulcblobs"></a>ulcBlobs

Debe establecerse en el número de elementos de la matriz pBlobs.

### <a name="pblobs"></a>pBlobs

Apunta a una matriz de ODJ_BLOB estructura.

## <a name="see-also"></a>Vea también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)

[**BLOB \_ DE ODJ**](odj-odj_blob.md)


