---
title: OP_PACKAGE_PART_COLLECTION
description: Definición de OP_PACKAGE_PART_COLLECTION IDL
ms.assetid: a7abf011-0335-4869-b4d9-144b2f392241
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8eb61397045a382fe5933025a4eeda2f563e838
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "104078557"
---
# <a name="op_package_part_collection-structure"></a>Estructura de OP_PACKAGE_PART_COLLECTION

Especifica una estructura que contiene una matriz de estructuras OP_PACKAGE_PART.

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

Contiene una matriz de estructuras OP_PACKAGE_PART.

### <a name="extension"></a>Extensión

Reservado para uso futuro y debe establecerse en ceros.

## <a name="see-also"></a>Vea también

[**Definiciones IDL de unión a dominio sin conexión**](odj-idl.md)

[**\_elemento de paquete de OP \_**](odj-op_package_part.md)

[**BLOB de operaciones \_**](odj-op_blob.md)

