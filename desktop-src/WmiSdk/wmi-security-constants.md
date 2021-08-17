---
description: WMI comprueba los derechos de acceso de las aplicaciones y los scripts.
ms.assetid: f6808f50-a1fd-434f-8a42-efa3afbe7871
ms.tgt_platform: multiple
title: Constantes de seguridad wmi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2f3a8ff4727852637fe6e4b808f0b8d3a74c958808cb3beb7bc9df32b0c995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739422"
---
# <a name="wmi-security-constants"></a>Constantes de seguridad wmi

WMI comprueba los derechos de acceso de aplicaciones y scripts para objetos como espacios de nombres WMI, impresora, servicios, aplicaciones DCOM, archivos, recursos compartidos y otros objetos protegibles. El acceso a estos objetos protegibles se controla mediante entradas de control de acceso (ACE). Cada ACE contiene listas que designan a qué grupos o usuarios tienen acceso. Para obtener más información sobre las listas de control de acceso y seguridad (ACL, DACL o SACL), vea listas de Access Control [(ACL)](/windows/desktop/SecAuthZ/access-control-lists) y [descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptors).

Muchos métodos de proveedor de WMI que afectan a objetos protegibles requieren que el administrador habilite determinados privilegios. La versión del privilegio que use depende del lenguaje de programación , como se muestra en [**Constantes de privilegios**](privilege-constants.md).

Las constantes de seguridad se definen en los temas siguientes:

-   [**Constantes de seguridad de eventos**](event-security-constants.md)
-   [**Constantes de derechos de acceso a archivos y directorios**](file-and-directory-access-rights-constants.md)
-   [**Constantes de derechos de acceso de espacio de nombres**](namespace-access-rights-constants.md)
-   [**Constantes de marca ACE de espacio de nombres**](namespace-ace-flag-constants.md)
-   [**Constantes de tipo ACE de espacio de nombres**](namespace-ace-type-constants.md)
-   [**Constantes de privilegios**](privilege-constants.md)

 

 
