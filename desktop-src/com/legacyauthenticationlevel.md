---
title: LegacyAuthenticationLevel
description: Establece el nivel de autenticación predeterminado para las aplicaciones que no llaman a CoInitializeSecurity.
ms.assetid: e14d2203-c84e-46af-befd-d82ef1936c9d
keywords:
- Valor del Registro LegacyAuthenticationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6be9f562a543e4750695ec2bf967b5a261209aae70d0bf91269bc2a074a9e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096955"
---
# <a name="legacyauthenticationlevel"></a>LegacyAuthenticationLevel

Establece el nivel de autenticación predeterminado para las aplicaciones que no llaman [**a CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

> [!Caution]  
> No se recomienda cambiar este valor, ya que esto afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso y podrían impedir que funcionen correctamente. Si va a cambiar este valor para que afecte a la configuración de seguridad de una aplicación COM determinada, en su lugar debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM concreta. Para obtener más información sobre cómo establecer la seguridad de todo el proceso, vea [Establecer la seguridad de todo el proceso.](setting-processwide-security.md)

 

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyAuthenticationLevel = value
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor REG \_ WORD** equivalente a las constantes RPC \_ C \_ AUTHN \_ LEVEL.



| Valor | Constante                             |
|-------|--------------------------------------|
| 1     | RPC \_ C \_ AUTHN \_ LEVEL \_ NONE           |
| 2     | CONEXIÓN \_ DE NIVEL DE \_ AUTENTICACIÓN \_ DE \_ RPC C        |
| 3     | LLAMADA \_ DE NIVEL DE \_ AUTENTICACIÓN \_ DE \_ RPC C           |
| 4     | RPC \_ C \_ AUTHN \_ LEVEL \_ PKT            |
| 5     | RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ INTEGRITY |
| 6     | RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY   |



 

Si este valor del Registro no está presente, el nivel de autenticación predeterminado establecido por el sistema es 2 (RPC \_ C \_ AUTHN \_ CONNECT).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**AuthenticationLevel**](authenticationlevel.md)
</dt> <dt>

[Registro de servidores COM](registering-com-servers.md)
</dt> <dt>

[Establecer la seguridad de todo el proceso](setting-processwide-security.md)
</dt> </dl>

 

 




