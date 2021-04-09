---
title: LegacyAuthenticationLevel
description: Establece el nivel de autenticación predeterminado para las aplicaciones que no llaman a CoInitializeSecurity.
ms.assetid: e14d2203-c84e-46af-befd-d82ef1936c9d
keywords:
- Valor del registro LegacyAuthenticationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d87d808287418f635629e15324f2f517619be6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076372"
---
# <a name="legacyauthenticationlevel"></a>LegacyAuthenticationLevel

Establece el nivel de autenticación predeterminado para las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

> [!Caution]  
> No se recomienda cambiar este valor, ya que esto afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso y podrían impedir que funcionen correctamente. Si va a cambiar este valor para que afecte a la configuración de seguridad de una aplicación COM determinada, debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM en particular. Para obtener más información sobre cómo establecer la seguridad de todo el proceso, consulte [configuración de la seguridad de todo el proceso](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyAuthenticationLevel = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **\_ palabra de registro** equivalente a las \_ constantes de nivel de autenticación de RPC C \_ \_ .



| Valor | Constante                             |
|-------|--------------------------------------|
| 1     | nivel de autenticación de RPC \_ C \_ \_ \_ ninguno           |
| 2     | \_conexión de \_ nivel de \_ autenticación \_ de RPC C        |
| 3     | \_llamada de \_ nivel de \_ autenticación \_ de RPC C           |
| 4     | \_PKT de \_ nivel de \_ autenticación \_ de RPC C            |
| 5     | integridad de la PKT de nivel de autenticación de RPC \_ C \_ \_ \_ \_ |
| 6     | \_privacidad de \_ nivel de \_ autenticación \_ de RPC C \_   |



 

Si este valor del registro no está presente, el nivel de autenticación predeterminado establecido por el sistema es 2 (RPC \_ C \_ authn \_ Connect).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**AuthenticationLevel**](authenticationlevel.md)
</dt> <dt>

[Registrar servidores COM](registering-com-servers.md)
</dt> <dt>

[Establecer la seguridad de todo el proceso](setting-processwide-security.md)
</dt> </dl>

 

 




