---
title: Proveedor LDAP de ADSI
description: El proveedor LDAP de ADSI implementa un conjunto de objetos ADSI que admiten diversas interfaces ADSI. Para tener acceso al proveedor LDAP, enlace con cualquiera de los objetos LDAP de ADSI mediante la ADsPath de LDAP.
ms.assetid: 3c13ea2f-fe40-4fd4-8540-422f277e07c1
ms.tgt_platform: multiple
keywords:
- Proveedor LDAP de ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8edbca53708a46c2f788c328a78bd2488973486
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903082"
---
# <a name="adsi-ldap-provider"></a>Proveedor LDAP de ADSI

El proveedor LDAP de ADSI implementa un conjunto de objetos ADSI que admiten diversas interfaces ADSI. Para tener acceso al proveedor LDAP, enlace con cualquiera de los objetos LDAP de ADSI mediante la ADsPath de LDAP.

Debe tener Adsldp.dll, Adsldpc.dll, Adsmsext.dll y Activeds.dll instalados en el equipo cliente para que funcionen con el proveedor.

> [!Note]  
> No se puede suponer que el proveedor LDAP de ADSI predeterminado sea totalmente seguro para subprocesos. Los escritores de aplicaciones multiproceso deben coordinar correctamente el acceso entre subprocesos mediante el uso correcto de objetos de sincronización como semáforos, exclusiones mutuas, secciones críticas, etc.

 

 

 




