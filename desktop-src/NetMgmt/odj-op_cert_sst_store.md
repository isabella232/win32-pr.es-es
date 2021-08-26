---
title: OP_CERT_SST_STORE
description: OP_CERT_SST_STORE definición de IDL
ms.assetid: 6c44756e-29f9-48fc-b678-d2b1f0fb90d4
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 4104635ea845394251f28eea48a2b3c67063826f98dd4da71a8f9adda8fd14a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911555"
---
# <a name="op_cert_sst_store-structure"></a>OP_CERT_SST_STORE estructura

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

Contiene un identificador para el almacén de certificados de [**Ubicaciones del almacén del sistema.**](../seccrypto/system-store-locations.md)

### <a name="pstorename"></a>pStoreName

Contiene el nombre del almacén.

### <a name="cbsst"></a>cbSst

Contiene el tamaño de pSst en bytes.

### <a name="psst"></a>Psst

Contiene un almacén de certificados serializado (vea [**RFC 7292).**](https://tools.ietf.org/html/rfc7292)

## <a name="see-also"></a>Vea también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)