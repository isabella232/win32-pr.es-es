---
title: OP_PACKAGE_PART_COLLECTION
description: OP_PACKAGE_PART_COLLECTION definición de IDL
ms.assetid: a7abf011-0335-4869-b4d9-144b2f392241
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 26a664bc05cc076ac6e4fb945c5381fd5d7075ec6653c807230cc97a7db135f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983426"
---
# <a name="op_package_part_collection-structure"></a>OP_PACKAGE_PART_COLLECTION estructura

Especifica una estructura que contiene una matriz de OP_PACKAGE_PART estructura.

## <a name="syntax"></a>Sintaxis

```C++
typedef struct _OP_PACKAGE_PART_COLLECTION
{
    ULONG                                 cParts;
    [size_is(cParts)]   POP_PACKAGE_PART  pParts;
    OP_BLOB                               Extension;
} OP_PACKAGE_PART_COLLECTION, *POP_PACKAGE_PART_COLLECTION;
```

## <a name="members"></a>Miembros

### <a name="cparts"></a>cParts

Contiene el número de elementos de pParts.

### <a name="pparts"></a>pParts

Contiene una matriz de OP_PACKAGE_PART estructura.

### <a name="extension"></a>Extensión

Reservado para uso futuro y DEBE establecerse en todos los ceros.

## <a name="see-also"></a>Vea también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)

[**PARTE DEL \_ PAQUETE \_ DE OPERACIÓN**](odj-op_package_part.md)

[**BLOB DE \_ OPERACIÓN**](odj-op_blob.md)

