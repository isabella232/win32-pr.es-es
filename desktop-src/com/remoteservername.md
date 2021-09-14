---
title: RemoteServerName
description: Configura el cliente para solicitar que el objeto se ejecute en un equipo determinado cada vez que se llama a una función de activación para la que no se especifica una estructura COSERVERINFO.
ms.assetid: 0413564e-e8ba-4e6e-ad29-62997c63aab3
keywords:
- Valor del Registro RemoteServerName COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0634d858b04fbbdf5d3a6024dbd9fdea4ee06d99
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060896"
---
# <a name="remoteservername"></a>RemoteServerName

Configura el cliente para solicitar que el objeto se ejecute en un equipo determinado cada vez que se llama a una función de activación para la que no se especifica una estructura [**COSERVERINFO.**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RemoteServerName = name
```

## <a name="remarks"></a>Observaciones

**RemoteServerName permite** la administración de configuración simple de aplicaciones cliente; se pueden escribir sin nombres de servidor codificados de forma hard-code y se pueden configurar modificando los valores del Registro **RemoteServerName** de las clases de objetos que usan.

Como se describe en la documentación de la enumeración [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) y la estructura [**COSERVERINFO,**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) uno de los parámetros de la activación COM distribuida es un puntero a una **estructura COSERVERINFO.** Cuando este valor no es **NULL**, la información de la estructura **COSERVERINFO** invalida el valor de la clave **RemoteServerName** para la llamada de función.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de servidores COM](registering-com-servers.md)
</dt> </dl>

 

 