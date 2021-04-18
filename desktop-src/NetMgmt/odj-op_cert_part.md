---
title: OP_CERT_PART
description: Definición de OP_CERT_PART IDL
ms.assetid: 30492801-f26e-447f-bcbf-d1108e7ae524
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: feb4f05171204442085f7d69691aa010d13e6042
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "105720191"
---
# <a name="op_cert_part-structure"></a>Estructura de OP_CERT_PART

Contiene los almacenes de certificados y PFX serializados.

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

## <a name="members"></a>Miembros

### <a name="cpfxstores"></a>cPfxStores

Contiene el número de elementos de pPfxStores.

### <a name="ppfxstores"></a>pPfxStores

Contiene una matriz de estructuras OP_CERT_PFX_STORE.

### <a name="csststores"></a>cSstStores

Contiene el número de elementos de pSstStores.

### <a name="psststores"></a>pSstStores

Contiene una matriz de estructuras OP_CERT_SST_STORE.

### <a name="extension"></a>Extensión

Reservado para uso futuro y debe contener ceros.

## <a name="see-also"></a>Vea también

[**Definiciones IDL de unión a dominio sin conexión**](odj-idl.md)

[**\_ \_ almacén pfx del certificado de OP \_**](odj-op_cert_pfx_store.md)

[**\_ \_ almacén SST del certificado de OP \_**](odj-op_cert_sst_store.md)

[**BLOB de operaciones \_**](odj-op_blob.md)

