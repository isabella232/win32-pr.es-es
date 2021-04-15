---
description: Interfaces utilizadas con cuotas de disco.
ms.assetid: 422d93d9-f4aa-428d-94c1-fdf2dcf4c974
title: Interfaces de cuota de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bbcd4240a6a5910942aad71c7ea080da40918a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497969"
---
# <a name="disk-quota-interfaces"></a>Interfaces de cuota de disco

Las siguientes interfaces se utilizan con cuotas de disco.



| Interfaz                                          | Descripción                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IDiskQuotaControl**](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)     | Controla las instalaciones de cuota de disco de un solo volumen del sistema de archivos NTFS.<br/>                             |
| [**IDiskQuotaEvents**](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)       | Recibe notificaciones de eventos relacionados con la cuota.<br/>                                                         |
| [**IDiskQuotaUser**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)           | Representa una única entrada de cuota de usuario en el archivo de información de cuota de volumen.<br/>                          |
| [**IDiskQuotaUserBatch**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch) | Agrega varios objetos de usuario de cuota a un contenedor que se envía para su actualización en una sola llamada.<br/> |
| [**IEnumDiskQuotaUsers**](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers) | Enumera las entradas de cuota de usuario en el volumen.<br/>                                                        |



 

 

