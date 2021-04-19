---
title: OP_PACKAGE
description: Definición de OP_PACKAGE IDL
ms.assetid: 065266a6-6db5-4113-bd2b-22ac6063236d
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 6220b3815ad6ff360af7255a91fc34d71125f38c
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "105720188"
---
# <a name="op_package-structure"></a>Estructura de OP_PACKAGE

Contiene una estructura que contiene un OP_PACKAGE_COLLECTION serializado.

## <a name="syntax"></a>Sintaxis

```C++
typedef struct _OP_PACKAGE
{
    GUID    EncryptionType;
    OP_BLOB EncryptionContext;
    OP_BLOB WrappedPartCollection;
    ULONG   cbDecryptedPartCollection;
    OP_BLOB Extension;
} OP_PACKAGE, *POP_PACKAGE;
```

## <a name="members"></a>Miembros

### <a name="encryptiontype"></a>EncryptionType

Reservado para uso futuro y debe establecerse en GUID_NULL.

### <a name="encryptioncontext"></a>EncryptionContext

Reservado para uso futuro y debe establecerse en ceros.

### <a name="wrappedpartcollection"></a>WrappedPartCollection

OP_BLOB estructura que contiene una estructura de OP_PACKAGE_COLLECTION serializada.

### <a name="cbdecryptedpartcollection"></a>cbDecryptedPartCollection

Reservado para uso futuro y debe establecerse en cero.

### <a name="extension"></a>Extensión

Reservado para uso futuro y debe establecerse en ceros.

## <a name="see-also"></a>Vea también

[**Definiciones IDL de unión a dominio sin conexión**](odj-idl.md)

[**BLOB de operaciones \_**](odj-op_blob.md)

[**\_colección de paquetes de OP \_**](odj-op_package_collection.md)
