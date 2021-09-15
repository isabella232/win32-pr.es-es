---
title: LegacyImpersonationLevel
description: Establece el nivel predeterminado de suplantación para las aplicaciones que no llaman a CoInitializeSecurity.
ms.assetid: 3f42c6d7-729d-4406-9391-4bfe28f7a59d
keywords:
- Valor del Registro LegacyImpersonationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74fa00494eb71e49c35bfa37b434afc5c999e73e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359839"
---
# <a name="legacyimpersonationlevel"></a>LegacyImpersonationLevel

Establece el nivel predeterminado de suplantación para las aplicaciones que no llaman [**a CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

> [!Caution]  
> No se recomienda cambiar este valor, ya que esto afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso y podrían impedir que funcionen correctamente. Si va a cambiar este valor para que afecte a la configuración de seguridad de una aplicación COM determinada, en su lugar debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM concreta. Para obtener más información sobre cómo establecer la seguridad de todo el proceso, vea [Establecer la seguridad de todo el proceso.](setting-processwide-security.md)

 

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
| 4     | DELEGADO \_ DE NIVEL DE IMP \_ \_ de \_ RPC C    |



 

Si este valor del Registro no está presente, el nivel de suplantación predeterminado establecido por el sistema es 2 (RPC \_ C \_ IMP LEVEL \_ \_ IDENTIFY).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de servidores COM](registering-com-servers.md)
</dt> <dt>

[Establecer la seguridad de todo el proceso](setting-processwide-security.md)
</dt> </dl>

 

 




