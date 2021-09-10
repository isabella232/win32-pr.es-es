---
title: LegacyImpersonationLevel
description: Establece el nivel predeterminado de suplantación para las aplicaciones que no llaman a CoInitializeSecurity.
ms.assetid: 3f42c6d7-729d-4406-9391-4bfe28f7a59d
keywords:
- Valor del Registro COM de LegacyImpersonationLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74fa00494eb71e49c35bfa37b434afc5c999e73e
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369639"
---
# <a name="legacyimpersonationlevel"></a>LegacyImpersonationLevel

Establece el nivel predeterminado de suplantación para las aplicaciones que no llaman a [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

> [!Caution]  
> No se recomienda cambiar este valor, ya que afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad para todo el proceso y podrían impedir que funcionen correctamente. Si va a cambiar este valor para que afecte a la configuración de seguridad de una aplicación COM determinada, en su lugar debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM concreta. Para obtener más información sobre cómo establecer la seguridad de todo el proceso, vea [Establecer la seguridad en todo el proceso.](setting-processwide-security.md)

 

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyImpersonationLevel = value
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor REG \_ WORD** equivalente a las constantes RPC \_ C IMP \_ \_ LEVEL.



| Valor | Constante                        |
|-------|---------------------------------|
| 1     | RPC \_ C \_ IMP \_ LEVEL \_ ANONYMOUS   |
| 2     | RPC \_ C \_ IMP \_ LEVEL \_ IDENTIFY    |
| 3     | \_SUPLANTACIÓN DE NIVEL DE IMP \_ \_ \_ DE RPC C |
| 4     | RPC \_ C \_ IMP \_ LEVEL \_ DELEGATE    |



 

Si este valor del Registro no está presente, el nivel de suplantación predeterminado establecido por el sistema es 2 (RPC \_ C \_ IMP LEVEL \_ \_ IDENTIFY).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de servidores COM](registering-com-servers.md)
</dt> <dt>

[Establecer la seguridad en todo el proceso](setting-processwide-security.md)
</dt> </dl>

 

 




