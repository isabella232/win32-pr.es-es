---
title: LegacyImpersonationLevel
description: Establece el nivel de suplantación predeterminado para las aplicaciones que no llaman a CoInitializeSecurity.
ms.assetid: 3f42c6d7-729d-4406-9391-4bfe28f7a59d
keywords:
- Valor del registro LegacyImpersonationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74fa00494eb71e49c35bfa37b434afc5c999e73e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704679"
---
# <a name="legacyimpersonationlevel"></a>LegacyImpersonationLevel

Establece el nivel de suplantación predeterminado para las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

> [!Caution]  
> No se recomienda cambiar este valor, ya que esto afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso y podrían impedir que funcionen correctamente. Si va a cambiar este valor para que afecte a la configuración de seguridad de una aplicación COM determinada, debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM en particular. Para obtener más información sobre cómo establecer la seguridad de todo el proceso, consulte [configuración de la seguridad de todo el proceso](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyImpersonationLevel = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **\_ palabra de registro** equivalente a las \_ \_ constantes de nivel Imp de RPC C \_ .



| Valor | Constante                        |
|-------|---------------------------------|
| 1     | \_nivel Imp de RPC C \_ \_ \_ anónimo   |
| 2     | \_identidad de \_ \_ nivel IMP \_ de RPC C    |
| 3     | \_ \_ \_ Impersonate de nivel IMP \_ de RPC C |
| 4     | \_delegado de \_ \_ nivel IMP \_ de RPC C    |



 

Si este valor del registro no está presente, el nivel de suplantación predeterminado establecido por el sistema es 2 (se identifica el nivel de Imp de RPC \_ C \_ \_ \_ ).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registrar servidores COM](registering-com-servers.md)
</dt> <dt>

[Establecer la seguridad de todo el proceso](setting-processwide-security.md)
</dt> </dl>

 

 




