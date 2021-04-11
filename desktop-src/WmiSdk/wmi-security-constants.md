---
description: WMI comprueba los derechos de acceso de las aplicaciones y los scripts.
ms.assetid: f6808f50-a1fd-434f-8a42-efa3afbe7871
ms.tgt_platform: multiple
title: Constantes de seguridad de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d360aa57c12c958db95c4b94f2b06327a3f70dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278971"
---
# <a name="wmi-security-constants"></a>Constantes de seguridad de WMI

WMI comprueba los derechos de acceso de las aplicaciones y los scripts para objetos como los espacios de nombres WMI, la impresora, los servicios, las aplicaciones DCOM, los archivos, los recursos compartidos y otros objetos protegibles. El acceso a estos objetos protegibles se controla mediante entradas de control de acceso (ACE). Cada ACE contiene listas que designan qué grupos o usuarios tienen acceso. Para obtener más información sobre la seguridad y las listas de control de acceso (ACL, DACL o SACL), consulte [listas de Access Control (ACL)](/windows/desktop/SecAuthZ/access-control-lists) y [descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptors).

Muchos métodos de proveedor de WMI que afectan a los objetos protegibles requieren que el administrador habilite determinados privilegios. La versión del privilegio que use depende del lenguaje de programación, como se muestra en [**constantes de privilegios**](privilege-constants.md).

Las constantes de seguridad se definen en los temas siguientes:

-   [**Constantes de seguridad de eventos**](event-security-constants.md)
-   [**Constantes de derechos de acceso a archivos y directorios**](file-and-directory-access-rights-constants.md)
-   [**Constantes de derechos de acceso de espacio de nombres**](namespace-access-rights-constants.md)
-   [**Constantes de marca ACE de espacio de nombres**](namespace-ace-flag-constants.md)
-   [**Constantes de tipo ACE de espacio de nombres**](namespace-ace-type-constants.md)
-   [**Constantes de privilegio**](privilege-constants.md)

 

 
