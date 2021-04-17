---
title: LegacySecureReferences
description: Determina si las invocaciones de AddRef/Release están protegidas para las aplicaciones que no llaman a CoInitializeSecurity.
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- Valor del registro LegacySecureReferences COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2776bf3661013f1e622bbc2e1c553f2551c62808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704680"
---
# <a name="legacysecurereferences"></a>LegacySecureReferences

Determina si  / las invocaciones de **liberación** de AddRef están protegidas para las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a>Observaciones

Este es un valor de **reg \_ SZ** . Un valor de ' Y ' o ' y ' indica que **AddRef** y **Release** están protegidos. Si este valor del registro no está presente o está establecido en un valor distinto de ' Y ' o ' y ', **AddRef** y **Release** no se protegen. Al habilitar las referencias seguras, se ralentizan las llamadas remotas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registrar servidores COM](registering-com-servers.md)
</dt> <dt>

[Establecer la seguridad de todo el proceso](setting-processwide-security.md)
</dt> </dl>

 

 




