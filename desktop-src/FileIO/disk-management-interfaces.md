---
description: Interfaces usadas en la administración de discos.
ms.assetid: c1f79e2e-834b-41dc-a15f-6dd1034d021b
title: Interfaces de administración de discos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a7314de976b1a5228a8b537da5d09be3df66936ed57915d86d78b0a84c4361e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823215"
---
# <a name="disk-management-interfaces"></a>Interfaces de administración de discos

Las interfaces siguientes se usan en la administración de discos.

## <a name="in-this-section"></a>En esta sección



| Interfaz                                                     | Descripción                                                                                                    |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IDiskQuotaControl**](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)<br/>     | Controla las instalaciones de cuota de disco de un único volumen del sistema de archivos NTFS.<br/>                             |
| [**IDiskQuotaEvents**](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)<br/>       | Recibe notificaciones de eventos relacionadas con la cuota.<br/>                                                         |
| [**IDiskQuotaUser**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)<br/>           | Representa una entrada de cuota de usuario única en el archivo de información de cuota de volumen.<br/>                          |
| [**IDiskQuotaUserBatch**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch)<br/> | Agrega varios objetos de usuario de cuota a un contenedor que, a continuación, se envía para su actualización en una sola llamada.<br/> |
| [**IEnumDiskQuotaUsers**](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers)<br/> | Enumera las entradas de cuota de usuario en el volumen.<br/>                                                        |



 

 

