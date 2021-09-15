---
title: LegacySecureReferences
description: Determina si las invocaciones AddRef/Release están protegidas para las aplicaciones que no llaman a CoInitializeSecurity.
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- Valor del Registro LegacySecureReferences COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2776bf3661013f1e622bbc2e1c553f2551c62808
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359836"
---
# <a name="legacysecurereferences"></a>LegacySecureReferences

Determina si las **invocaciones addRef** Release están protegidas /  para las aplicaciones que no llaman [**a CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG SZ.** Un valor de "Y" o "y" indica que **AddRef** y **Release están** protegidos. Si este valor del Registro no está presente o está establecido en un valor distinto de "Y" o **"y", AddRef** y **Release** no están protegidos. La habilitación de referencias seguras ralentiza las llamadas remotas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de servidores COM](registering-com-servers.md)
</dt> <dt>

[Establecer la seguridad de todo el proceso](setting-processwide-security.md)
</dt> </dl>

 

 




