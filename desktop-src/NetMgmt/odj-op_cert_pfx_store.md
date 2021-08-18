---
title: OP_CERT_PFX_STORE
description: OP_CERT_PFX_STORE definición de IDL
ms.assetid: 10773feb-623c-4256-a973-f006ed66d936
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 28e8b9e1a6d73f3d93e1700f812b21a0edf21982b7d5b9c927f4e7391b961850
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911545"
---
# <a name="op_cert_pfx_store-structure"></a>OP_CERT_PFX_STORE estructura

Contiene una estructura PFX serializada.

## <a name="syntax"></a>Sintaxis

```C++
typedef struct _OP_CERT_PFX_STORE
{
    [string] wchar_t            *pTemplateName;
    ULONG                       ulPrivateKeyExportPolicy;
    [string] wchar_t            *pPolicyServerUrl;
    ULONG                       ulPolicyServerUrlFlags;
    [string] wchar_t            *pPolicyServerId;
    ULONG                       cbPfx;
    [size_is(cbPfx)]    PBYTE   pPfx;
} OP_CERT_PFX_STORE, *POP_CERT_PFX_STORE;
```

## <a name="members"></a>Miembros

### <a name="ptemplatename"></a>pTemplateName

Debe establecerse en el nombre de la plantilla de certificado utilizada para crear el certificado.

### <a name="ulprivatekeyexportpolicy"></a>ulPrivateKeyExportPolicy

Contiene un valor de la [**enumeración X509PrivateKeyExportFlags.**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags)

### <a name="ppolicyserverurl"></a>pPolicyServerUrl

Debe establecerse la dirección URL del servidor de directivas.

### <a name="ulpolicyserverurlflags"></a>ulPolicyServerUrlFlags

Contiene un valor de la [**enumeración PolicyServerUrlFlags.**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags)

### <a name="ppolicyserverid"></a>pPolicyServerId

Contiene una cadena que identifica de forma única el servidor de directivas.

### <a name="cbpfx"></a>cbPfx

Contiene el tamaño de pPfx en bytes.

### <a name="ppfx"></a>pPfx

Contiene una estructura PFX serializada (vea [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).

## <a name="see-also"></a>Vea también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)
