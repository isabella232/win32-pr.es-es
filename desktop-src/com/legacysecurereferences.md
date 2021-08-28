---
title: LegacySecureReferences
description: Determina si las invocaciones AddRef/Release están protegidas para las aplicaciones que no llaman a CoInitializeSecurity.
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- Valor del Registro COM de LegacySecureReferences
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3a4ab964d73fa4b194c734f28c23ff068239370088c090051464129b6caf14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736552"
---
# <a name="legacysecurereferences"></a>LegacySecureReferences

Determina si las **invocaciones addRef** Release están protegidas /  para las aplicaciones que no llaman [**a CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ SZ reg.** Un valor de "Y" o "y" indica que **AddRef** **y Release están** protegidos. Si este valor del Registro no está presente o se establece en un valor distinto de "Y" o "y", **AddRef** y **Release** no están protegidos. La habilitación de referencias seguras ralentiza las llamadas remotas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de servidores COM](registering-com-servers.md)
</dt> <dt>

[Establecer la seguridad en todo el proceso](setting-processwide-security.md)
</dt> </dl>

 

 




