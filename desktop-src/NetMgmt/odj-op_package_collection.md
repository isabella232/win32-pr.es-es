---
title: OP_PACKAGE_PART_COLLECTION
description: OP_PACKAGE_PART_COLLECTION definición de IDL
ms.assetid: a7abf011-0335-4869-b4d9-144b2f392241
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8eb61397045a382fe5933025a4eeda2f563e838
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566901"
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

## <a name="members"></a>Members

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

