---
description: 'Para anunciar una aplicación según la instalación de cada usuario cuando la aplicación requiere privilegios elevados (es decir, sistema) para la instalación, siga las instrucciones de la lista siguiente:'
ms.assetid: 0d2bd2d9-0eac-4519-862c-15f0ee5cbc40
title: Anunciar una aplicación Per-User que se va a instalar con privilegios elevados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7d9888714f28282e060b3a1e7eea0291b4e0e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667048"
---
# <a name="advertising-a-per-user-application-to-be-installed-with-elevated-privileges"></a>Anunciar una aplicación Per-User que se va a instalar con privilegios elevados

Para anunciar una aplicación según la instalación de cada usuario cuando la aplicación requiere privilegios elevados (es decir, sistema) para la instalación, siga las instrucciones de la lista siguiente:

-   El proceso debe ser un servicio que se ejecute con la cuenta de sistema LocalSystem en Windows XP o posterior.
-   Genere un script de anuncio mediante una llamada a [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) o [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa).
-   El proceso debe suplantar al usuario que es el destino del anuncio.
-   Llame a [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)y use los \_ \| \_ \_ \| \_ \_ \| \_ métodos abreviados de marcas SCRIPTFLAGS CACHEINFO SCRIPTFLAGS REGDATA APPINFO SCRIPTFLAGS REGDATA CNFGINFO SCRIPTFLAGS.

Al seguir las instrucciones, se anuncia una aplicación a un usuario especificado y, cuando el usuario elige instalar, la aplicación se instala con privilegios elevados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicación de revisiones para aplicaciones administradas por usuario](patching-per-user-managed-applications.md)
</dt> </dl>

 

 



