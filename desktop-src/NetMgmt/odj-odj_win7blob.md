---
title: ODJ_WIN7BLOB
description: ODJ_WIN7BLOB definición de IDL
ms.assetid: 5802e00c-b943-45d8-8298-5c2b4b996b85
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: ab6f6582b23d6e65866ba1380b696fab6d8313578fab47ad5dda999b09a1caa7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911604"
---
# <a name="odj_win7blob-structure"></a>ODJ_WIN7BLOB estructura

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

Contiene información sobre el dominio que se va a unir.

### <a name="dcinfo"></a>DcInfo

Contiene información de nomenclatura y direccionamiento sobre el controlador de dominio que se usó para crear la cuenta de Active Directory.

### <a name="options"></a>Opciones

Debe establecerse en cero.

## <a name="see-also"></a>Vea también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)

[**INFORMACIÓN DE DOMINIO \_ DNS DE \_ DIRECTIVA \_ DE \_ ODJ**](odj-odj_policy_dns_domain_info.md)

[**DOMAIN_CONTROLLER_INFOW**](/windows/win32/api/dsgetdc/ns-dsgetdc-domain_controller_infow)



