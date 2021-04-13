---
title: OP_CERT_SST_STORE
description: Definición de OP_CERT_SST_STORE IDL
ms.assetid: 6c44756e-29f9-48fc-b678-d2b1f0fb90d4
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 294d21d730e1cce478088cddb43686706217ec5b
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "104421701"
---
# <a name="op_cert_sst_store-structure"></a>Estructura de OP_CERT_SST_STORE

Contiene un almacén de certificados serializado.

## <a name="syntax"></a>Sintaxis

```C++
typedef struct _OP_CERT_SST_STORE
{
    ULONG                       StoreLocation;
    [string] wchar_t            *pStoreName;
    ULONG                       cbSst;
    [size_is(cbSst)]    PBYTE   pSst;
} OP_CERT_SST_STORE, *POP_CERT_SST_STORE;
```

## <a name="members"></a>Miembros

### <a name="storelocation"></a>StoreLocation

Contiene un identificador para el almacén de certificados de las [**ubicaciones del almacén del sistema**](../seccrypto/system-store-locations.md).

### <a name="pstorename"></a>pStoreName

Contiene el nombre del almacén.

### <a name="cbsst"></a>cbSst

Contiene el tamaño de pSst en bytes.

### <a name="psst"></a>pSst

Contiene un almacén de certificados en serie (consulte [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).

## <a name="see-also"></a>Vea también

[**Definiciones IDL de unión a dominio sin conexión**](odj-idl.md)