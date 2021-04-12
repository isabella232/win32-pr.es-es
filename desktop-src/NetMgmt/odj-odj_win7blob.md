---
title: ODJ_WIN7BLOB
description: Definición de ODJ_WIN7BLOB IDL
ms.assetid: 5802e00c-b943-45d8-8298-5c2b4b996b85
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 2083648636bd58c64314ba22852839f89ed4461d
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "104359497"
---
# <a name="odj_win7blob-structure"></a>Estructura de ODJ_WIN7BLOB

Contiene la información básica necesaria para unir un cliente a un dominio.

## <a name="syntax"></a>Sintaxis

```C++
typedef struct _ODJ_WIN7BLOB
{
    [string] wchar_t *lpDomain;
    [string] wchar_t *lpMachineName;
    [string] wchar_t *lpMachinePassword;
    ODJ_POLICY_DNS_DOMAIN_INFO  DnsDomainInfo;
    DOMAIN_CONTROLLER_INFOW DcInfo;
    DWORD Options;
} ODJ_WIN7BLOB;
```

## <a name="members"></a>Miembros

### <a name="lpdomain"></a>lpDomain

Debe establecerse en el nombre de dominio.

### <a name="lpmachinename"></a>lpMachineName

Debe establecerse en el nombre de la máquina.

### <a name="lpmachinepassword"></a>lpMachinePassword

Debe establecerse en una contraseña de texto no cifrado para la cuenta de equipo identificada por lpMachineName

### <a name="dnsdomaininfo"></a>DnsDomainInfo

Contiene información sobre el dominio que se va a combinar.

### <a name="dcinfo"></a>DcInfo

Contiene información de nombre y dirección sobre el controlador de dominio que se usó para crear la cuenta de equipo Active Directory.

### <a name="options"></a>Opciones

Debe establecerse en cero.

## <a name="see-also"></a>Vea también

[**Definiciones IDL de unión a dominio sin conexión**](odj-idl.md)

[**\_información de \_ \_ dominio DNS de directiva \_ de ODJ**](odj-odj_policy_dns_domain_info.md)

[**DOMAIN_CONTROLLER_INFOW**](/windows/win32/api/dsgetdc/ns-dsgetdc-domain_controller_infow)



