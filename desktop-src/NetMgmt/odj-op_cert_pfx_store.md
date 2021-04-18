---
title: OP_CERT_PFX_STORE
description: Definición de OP_CERT_PFX_STORE IDL
ms.assetid: 10773feb-623c-4256-a973-f006ed66d936
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: b07d0b8e5572763cc42fe2f5b19a4dde2cfe2157
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "105720190"
---
# <a name="op_cert_pfx_store-structure"></a>Estructura de OP_CERT_PFX_STORE

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

Debe establecerse en el nombre de la plantilla de certificado que se usa para crear el certificado.

### <a name="ulprivatekeyexportpolicy"></a>ulPrivateKeyExportPolicy

Contiene un valor de la enumeración [**X509PrivateKeyExportFlags**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags) .

### <a name="ppolicyserverurl"></a>pPolicyServerUrl

Debe establecer la dirección URL del servidor de directivas.

### <a name="ulpolicyserverurlflags"></a>ulPolicyServerUrlFlags

Contiene un valor de la enumeración [**PolicyServerUrlFlags**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags) .

### <a name="ppolicyserverid"></a>pPolicyServerId

Contiene una cadena que identifica de forma única el servidor de directivas

### <a name="cbpfx"></a>cbPfx

Contiene el tamaño de pPfx en bytes.

### <a name="ppfx"></a>pPfx

Contiene una estructura PFX serializada (consulte [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).

## <a name="see-also"></a>Vea también

[**Definiciones IDL de unión a dominio sin conexión**](odj-idl.md)
