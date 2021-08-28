---
title: AuthenticationLevel
description: Establece el nivel de autenticación para las aplicaciones que no llaman a CoInitializeSecurity o para las aplicaciones que llaman a CoInitializeSecurity y especifican un AppID.
ms.assetid: 137cbffe-6f45-43f4-bf35-b064b3607fcc
keywords:
- Valor del Registro AuthenticationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7968382ea97243c1116dd6785be34a0d1c3e6eafc6cb9ee13f16b939029a6611
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120535"
---
# <a name="authenticationlevel"></a>AuthenticationLevel

Establece el nivel de autenticación para las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o para las aplicaciones que llaman a **CoInitializeSecurity** y especifican un AppID.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AuthenticationLevel = value
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ REG DWORD** equivalente a las constantes RPC \_ C \_ AUTHN \_ LEVEL.



| Valor | Constante                             |
|-------|--------------------------------------|
| 1     | RPC \_ C \_ AUTHN \_ LEVEL \_ NONE           |
| 2     | CONEXIÓN \_ DE NIVEL DE \_ AUTENTICACIÓN \_ DE \_ RPC C        |
| 3     | LLAMADA \_ DE NIVEL DE \_ AUTENTICACIÓN \_ DE \_ RPC C           |
| 4     | RPC \_ C \_ AUTHN \_ LEVEL \_ PKT            |
| 5     | INTEGRIDAD PKT DE NIVEL DE \_ \_ \_ \_ AUTENTICACIÓN RPC \_ C |
| 6     | RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY   |



 

El **valor AuthenticationLevel** es similar al [**valor LegacyAuthenticationLevel.**](legacyauthenticationlevel.md) Si el **valor AuthenticationLevel** está presente, se usa en lugar del **valor LegacyAuthenticationLevel** para ese AppID.

Si el **valor AuthenticationLevel** es del tipo incorrecto o está fuera del intervalo, se produce un error en [**CoInitializeSecurity,**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) lo que provoca un error en la serialización de la interfaz. Esto impide que la aplicación haga llamadas (entre departamentos, subprocesos, procesos cruzados o entre equipos).

Los **valores AuthenticationLevel** [**y AccessPermission**](accesspermission.md) son independientes. Si no hay uno, se usa el valor predeterminado. Las reglas siguientes enumeran la interacción entre el **valor AuthenticationLevel** y **el valor AccessPermission:**

-   Si **AuthenticationLevel** es NONE, se omiten los valores [**AccessPermission**](accesspermission.md) y [**DefaultAccessPermission**](defaultaccesspermission.md) (para esa aplicación).
-   Si **AuthenticationLevel** no está presente y [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) es NONE, se omiten los valores [**AccessPermission**](accesspermission.md) y [**DefaultAccessPermission**](defaultaccesspermission.md) (para esa aplicación).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de nivel de autenticación](com-authentication-level-constants.md)
</dt> <dt>

[**LegacyAuthenticationLevel**](legacyauthenticationlevel.md)
</dt> <dt>

[Registro de servidores COM](registering-com-servers.md)
</dt> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 




