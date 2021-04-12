---
description: Interfaces usadas en administración de discos.
ms.assetid: c1f79e2e-834b-41dc-a15f-6dd1034d021b
title: Interfaces de administración de discos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c86881ff3bf6232da68c4cf1539dbbedf87c50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278462"
---
# <a name="disk-management-interfaces"></a>Interfaces de administración de discos

En administración de discos se usan las siguientes interfaces.

## <a name="in-this-section"></a>En esta sección



| Interfaz                                                     | Descripción                                                                                                    |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IDiskQuotaControl**](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)<br/>     | Controla las instalaciones de cuota de disco de un solo volumen del sistema de archivos NTFS.<br/>                             |
| [**IDiskQuotaEvents**](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)<br/>       | Recibe notificaciones de eventos relacionados con la cuota.<br/>                                                         |
| [**IDiskQuotaUser**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)<br/>           | Representa una única entrada de cuota de usuario en el archivo de información de cuota de volumen.<br/>                          |
| [**IDiskQuotaUserBatch**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch)<br/> | Agrega varios objetos de usuario de cuota a un contenedor que se envía para su actualización en una sola llamada.<br/> |
| [**IEnumDiskQuotaUsers**](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers)<br/> | Enumera las entradas de cuota de usuario en el volumen.<br/>                                                        |



 

 

