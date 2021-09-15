---
title: OP_CERT_PART
description: OP_CERT_PART definición de IDL
ms.assetid: 30492801-f26e-447f-bcbf-d1108e7ae524
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: feb4f05171204442085f7d69691aa010d13e6042
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566925"
---
# <a name="op_cert_part-structure"></a>OP_CERT_PART estructura

Contiene pfx serializado y almacenes de certificados.

## <a name="syntax"></a>Sintaxis

```C++
typedef struct _OP_CERT_PART
{
    ULONG                                       cPfxStores;
    [size_is(cPfxStores)]   POP_CERT_PFX_STORE  pPfxStores;
    ULONG                                       cSstStores;
    [size_is(cSstStores)]   POP_CERT_SST_STORE  pSstStores;
    OP_BLOB                                     Extension;
} OP_CERT_PART, *POP_CERT_PART;
```

## <a name="members"></a>Members

### <a name="cpfxstores"></a>cPfxStores

Contiene el número de elementos de pPfxStores.

### <a name="ppfxstores"></a>pPfxStores

Contiene una matriz de OP_CERT_PFX_STORE estructura.

### <a name="csststores"></a>cSstStores

Contiene el número de elementos de pSstStores.

### <a name="psststores"></a>pSstStores

Contiene una matriz de OP_CERT_SST_STORE estructura.

### <a name="extension"></a>Extensión

Reservado para uso futuro y debe contener todos los ceros.

## <a name="see-also"></a>Vea también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)

[**OP \_ CERT \_ PFX \_ STORE**](odj-op_cert_pfx_store.md)

[**OP \_ CERT \_ SST \_ STORE**](odj-op_cert_sst_store.md)

[**BLOB DE \_ OPERACIÓN**](odj-op_blob.md)

