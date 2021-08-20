---
description: Las siguientes notificaciones se usan con las funciones SetupInstallFile, SetupInstallFileEx y SetupInstallFromInfSection. Para obtener más información sobre el formato y el uso de las notificaciones, vea Notificaciones.
ms.assetid: 095cf4c9-3cb9-4b95-a8a2-9312c134e721
title: Notificaciones de archivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b48aff261cd867b1d2f01dbcad79f6e8fdefe49b1cfbba8dd07bb6c4572354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117965499"
---
# <a name="inf-file-notifications"></a>Notificaciones de archivo INF

Las siguientes notificaciones se usan con las funciones [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)y [**SetupInstallFromInfSection.**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) Para obtener más información sobre el formato y el uso de las notificaciones, vea [Notificaciones](notifications.md).



| Notificación                                                      | Descripción                                                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**SPFILENOTIFY \_ FILEOPDELAYED**](spfilenotify-fileopdelayed.md) | El archivo está en uso y la operación actual se retrasa hasta que se reinicia el sistema. |
| [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md)   | El idioma del archivo actual no coincide con el idioma del sistema.                   |
| [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md)   | Ya existe una copia del archivo especificado en el destino.                             |
| [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md)     | Existe una versión más reciente del archivo especificado en el destino.                            |



 

> [!Note]  
> Dado [**que SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) crea y confirma una cola de archivos interna, también usa las notificaciones de [cola de archivos](file-queue-notifications.md).

 

 

 



