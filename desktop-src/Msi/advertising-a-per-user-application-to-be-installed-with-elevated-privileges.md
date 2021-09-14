---
description: 'Para anunciar una aplicación por instalación por usuario cuando la aplicación requiera privilegios elevados (es decir, del sistema) para la instalación, use las instrucciones de la lista siguiente:'
ms.assetid: 0d2bd2d9-0eac-4519-862c-15f0ee5cbc40
title: Anuncio de Per-User aplicación que se va a instalar con privilegios elevados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7d9888714f28282e060b3a1e7eea0291b4e0e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159166"
---
# <a name="advertising-a-per-user-application-to-be-installed-with-elevated-privileges"></a>Anuncio de Per-User aplicación que se va a instalar con privilegios elevados

Para anunciar una aplicación por instalación por usuario cuando la aplicación requiera privilegios elevados (es decir, del sistema) para la instalación, use las instrucciones de la lista siguiente:

-   El proceso debe ser un servicio que se ejecute en la cuenta del sistema LocalSystem Windows XP o posterior.
-   Genere un script de anuncio mediante una [**llamada a MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) [**o MsiAdvertiseProductEx.**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)
-   El proceso debe suplantar al usuario que es el destino del anuncio.
-   Llame [**a MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)y use las marcas SCRIPTFLAGS \_ CACHEINFO \| SCRIPTFLAGS \_ REGDATA \_ APPINFO \| SCRIPTFLAGS \_ REGDATA \_ CNFGINFO \| \_ SCRIPTFLAGS SHORTCUTS.

Al seguir las directrices, anuncia una aplicación a un usuario especificado y, cuando el usuario decide instalarla, la aplicación se instala con privilegios elevados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicación de revisiones para aplicaciones administradas por usuario](patching-per-user-managed-applications.md)
</dt> </dl>

 

 



