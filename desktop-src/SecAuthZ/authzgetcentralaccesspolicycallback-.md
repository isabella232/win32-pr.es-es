---
description: La función AuthzGetCentralAccessPolicyCallback es una función definida por la aplicación que recupera la Directiva de acceso central. AuthzGetCentralAccessPolicyCallback es un marcador de posición para el nombre de la función definida por la aplicación.
ms.assetid: 1D5831EF-ACA8-4EE9-A7C1-E1A3CB74CEC0
title: Función de devolución de llamada AuthzGetCentralAccessPolicyCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzGetCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b96832fa647fde920a70ac3d6608c8ebb0048892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653098"
---
# <a name="authzgetcentralaccesspolicycallback-callback-function"></a>Función de devolución de llamada AuthzGetCentralAccessPolicyCallback

La función *AuthzGetCentralAccessPolicyCallback* es una función definida por la aplicación que recupera la Directiva de acceso central. *AuthzGetCentralAccessPolicyCallback* es un marcador de posición para el nombre de la función definida por la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CALLBACK AuthzGetCentralAccessPolicyCallback (
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PSID                        capid,
  _In_opt_ PVOID                       pArgs,
  _Out_    PBOOL                       pCentralAccessPolicyApplicable,
  _Out_    PVOID                       ppCentralAccessPolicy
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hAuthzClientContext* \[ de\]
</dt> <dd>

Identificador del contexto de cliente.

</dd> <dt>

*capid* \[ de\]
</dt> <dd>

IDENTIFICADOR de la Directiva de acceso central que se va a recuperar.

</dd> <dt>

*pArgs* \[ en, opcional\]
</dt> <dd>

Argumentos opcionales que se pasaron a la función [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) a través del miembro **OptionalArguments** de la estructura de [**\_ \_ solicitud de acceso de AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_access_request) .

</dd> <dt>

*pCentralAccessPolicyApplicable* \[ enuncia\]
</dt> <dd>

Puntero a un valor booleano que el administrador de recursos utiliza para indicar si se debe usar una directiva de acceso central durante la evaluación del acceso.

</dd> <dt>

*ppCentralAccessPolicy* \[ enuncia\]
</dt> <dd>

Puntero a la Directiva de acceso central (CAP) que se va a usar para evaluar el acceso. Si este valor es **null**, se aplica el límite predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve **true**.

Si la función no puede realizar la evaluación, devuelve **false**. Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para devolver un error a la función de comprobación de acceso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                   |
| Redistribuible<br/>          | Paquete de herramientas de administración de Windows Server 2003 en Windows XP<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_solicitud de acceso de AUTHZ \_**](/windows/desktop/api/Authz/ns-authz-authz_access_request)
</dt> <dt>

[**AUTHZ \_ init \_ info**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> </dl>

 

