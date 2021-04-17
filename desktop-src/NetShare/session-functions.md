---
description: Las funciones de sesión de administración de red controlan las sesiones de red establecidas entre estaciones de trabajo y servidores. Las funciones requieren que se inicie el servicio servidor en el servidor.
ms.assetid: 931455e3-1301-4a68-93c3-2674b3d4c491
title: Funciones de sesión (administración de recursos compartidos de red)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c672abd7c976cb9f83fa4f387dd40d175879dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677665"
---
# <a name="session-functions-network-share-management"></a>Funciones de sesión (administración de recursos compartidos de red)

Las funciones de sesión de administración de red controlan las sesiones de red establecidas entre estaciones de trabajo y servidores. Las funciones requieren que se inicie el servicio servidor en el servidor.

A continuación se enumeran las funciones de sesión.



| Función                                       | Descripción                                                                                       |
|------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel)         | Elimina las conexiones actuales entre una estación de trabajo y un servidor. finaliza la sesión de red. |
| [**NetSessionEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netsessionenum)       | Devuelve información acerca de todas las sesiones actuales establecidas para un servidor.                          |
| [**NetSessionGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiongetinfo) | Devuelve información sobre una sesión determinada.                                                   |



 

Una *sesión* es un vínculo entre una estación de trabajo y un servidor. Una sesión se establece la primera vez que una estación de trabajo realiza una conexión a un recurso compartido en el servidor. Hasta que finalice la sesión, todas las conexiones posteriores entre la estación de trabajo y el servidor formarán parte de la misma sesión. Para finalizar una sesión, una aplicación en el extremo del servidor de una conexión llama a la función [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel) .

Las funciones de sesión de administración de red administran la información por usuario con el parámetro de *nombre de usuario* . Dado que puede haber varios usuarios por sesión, este parámetro es necesario para tener acceso a la información específica del usuario para la sesión.

Las funciones de sesión están disponibles en cinco niveles de información:

<dl>

[**Información de sesión \_ \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_0)  
[**Información de sesión \_ \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_1)  
[**Información de sesión \_ \_ 2**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_2)  
[**Información de la sesión \_ \_ 10**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_10)  
[**Información de sesión \_ \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_502)  
</dl>

Si programa para Active Directory, es posible que pueda llamar a determinados métodos de la interfaz de servicio Active Directory (ADSI) para lograr la misma funcionalidad que puede lograr mediante una llamada a las funciones de sesión de administración de red. Para obtener más información, vea [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) y [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).

 

 
