---
title: AuthenticationLevel
description: Establece el nivel de autenticación para las aplicaciones que no llaman a CoInitializeSecurity o para las aplicaciones que llaman a CoInitializeSecurity y especifican un AppID.
ms.assetid: 137cbffe-6f45-43f4-bf35-b064b3607fcc
keywords:
- Valor del registro AuthenticationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b04bcf4992c8a6943bcb515fa0a4eae616fec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357762"
---
# <a name="authenticationlevel"></a>AuthenticationLevel

Establece el nivel de autenticación para las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o para las aplicaciones que llaman a **CoInitializeSecurity** y especifican un AppID.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AuthenticationLevel = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **Registro \_ DWORD** equivalente a las constantes de nivel de autenticación de RPC \_ C \_ \_ .



| Valor | Constante                             |
|-------|--------------------------------------|
| 1     | nivel de autenticación de RPC \_ C \_ \_ \_ ninguno           |
| 2     | \_conexión de \_ nivel de \_ autenticación \_ de RPC C        |
| 3     | \_llamada de \_ nivel de \_ autenticación \_ de RPC C           |
| 4     | \_PKT de \_ nivel de \_ autenticación \_ de RPC C            |
| 5     | integridad de la PKT de nivel de autenticación de RPC \_ C \_ \_ \_ \_ |
| 6     | \_privacidad de \_ nivel de \_ autenticación \_ de RPC C \_   |



 

El valor **AuthenticationLevel** es similar al valor [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) . Si el valor **AuthenticationLevel** está presente, se usa en lugar del valor **LegacyAuthenticationLevel** para ese AppID.

Si el valor de **AuthenticationLevel** es del tipo incorrecto o está fuera del intervalo, se produce un error en [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) , lo que provoca un error en la serialización de la interfaz. Esto evita que la aplicación realice llamadas en todo (entre apartamentos, entre subprocesos, entre procesos o entre equipos).

Los valores **AuthenticationLevel** y [**AccessPermission**](accesspermission.md) son independientes. Si no hay ninguno, se usa el valor predeterminado. Las siguientes reglas muestran la interacción entre el valor de **AuthenticationLevel** y el valor de **AccessPermission** :

-   Si **AuthenticationLevel** es None, se omiten los valores [**AccessPermission**](accesspermission.md) y [**DefaultAccessPermission**](defaultaccesspermission.md) (para esa aplicación).
-   Si **AuthenticationLevel** no está presente y [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) es None, se omiten los valores [**AccessPermission**](accesspermission.md) y [**DefaultAccessPermission**](defaultaccesspermission.md) (para esa aplicación).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de nivel de autenticación](com-authentication-level-constants.md)
</dt> <dt>

[**LegacyAuthenticationLevel**](legacyauthenticationlevel.md)
</dt> <dt>

[Registrar servidores COM](registering-com-servers.md)
</dt> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 




