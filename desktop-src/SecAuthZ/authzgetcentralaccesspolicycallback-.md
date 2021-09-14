---
description: La función AuthzGetCentralAccessPolicyCallback es una función definida por la aplicación que recupera la directiva de acceso central. AuthzGetCentralAccessPolicyCallback es un marcador de posición para el nombre de la función definida por la aplicación.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168982"
---
# <a name="authzgetcentralaccesspolicycallback-callback-function"></a>Función de devolución de llamada AuthzGetCentralAccessPolicyCallback

La *función AuthzGetCentralAccessPolicyCallback* es una función definida por la aplicación que recupera la directiva de acceso central. *AuthzGetCentralAccessPolicyCallback es* un marcador de posición para el nombre de la función definida por la aplicación.

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

*hAuthzClientContext* \[ En\]
</dt> <dd>

Controlar el contexto de cliente.

</dd> <dt>

*capid* \[ En\]
</dt> <dd>

Identificador de la directiva de acceso central que se recuperará.

</dd> <dt>

*pArgs* \[ en, opcional\]
</dt> <dd>

Argumentos opcionales que se pasaron a la función [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) a través del **miembro OptionalArguments** de la estructura [**ACCESS REQUEST \_ \_ de AUTHZ.**](/windows/desktop/api/Authz/ns-authz-authz_access_request)

</dd> <dt>

*pCentralAccessPolicyApplicable* \[ out\]
</dt> <dd>

Puntero a un valor booleano que el administrador de recursos usa para indicar si se debe usar una directiva de acceso central durante la evaluación de acceso.

</dd> <dt>

*ppCentralAccessPolicy* \[ out\]
</dt> <dd>

Puntero a la directiva de acceso central (CAP) que se usará para evaluar el acceso. Si este valor es **NULL,** se aplica el CAP predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve **TRUE.**

Si la función no puede realizar la evaluación, devuelve **FALSE**. Use [**SetLastError para**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) devolver un error a la función de comprobación de acceso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                             |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                   |
| Redistribuible<br/>          | Windows Paquete de herramientas de administración de Server 2003 en Windows XP<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SOLICITUD DE ACCESO \_ DE \_ AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_access_request)
</dt> <dt>

[**INFORMACIÓN DE \_ AUTHZ INIT \_**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> </dl>

 

