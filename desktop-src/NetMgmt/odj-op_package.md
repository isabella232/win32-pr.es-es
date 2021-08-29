---
title: OP_PACKAGE
description: OP_PACKAGE definición de IDL
ms.assetid: 065266a6-6db5-4113-bd2b-22ac6063236d
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 81fdc237b731489f7ac501a4e053e62d744b0fdef77c5b630cd478dede5aeda5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911495"
---
# <a name="op_package-structure"></a>OP_PACKAGE estructura

Contiene una estructura que contiene una estructura OP_PACKAGE_COLLECTION.

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

Reservado para uso futuro y DEBE establecerse en GUID_NULL.

### <a name="encryptioncontext"></a>EncryptionContext

Reservado para uso futuro y DEBE establecerse en todos los ceros.

### <a name="wrappedpartcollection"></a>WrappedPartCollection

Estructura OP_BLOB que contiene una estructura OP_PACKAGE_COLLECTION serializada.

### <a name="cbdecryptedpartcollection"></a>cbDecryptedPartCollection

Reservado para uso futuro y DEBE establecerse en cero.

### <a name="extension"></a>Extensión

Reservado para uso futuro y DEBE establecerse en todos los ceros.

## <a name="see-also"></a>Vea también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)

[**BLOB DE \_ OPERACIÓN**](odj-op_blob.md)

[**COLECCIÓN DE \_ PAQUETES \_ DE OPERACIÓN**](odj-op_package_collection.md)
