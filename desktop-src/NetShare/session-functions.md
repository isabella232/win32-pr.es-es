---
description: Comprenda las funciones de sesión en la administración de recursos compartidos de red. Estas funciones controlan las sesiones de red establecidas entre estaciones de trabajo y servidores.
ms.assetid: 931455e3-1301-4a68-93c3-2674b3d4c491
title: Funciones de sesión (Administración de recursos compartidos de red)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdde451eb2942171569b24c36aae5d5742208e5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409728"
---
# <a name="session-functions-network-share-management"></a>Funciones de sesión (Administración de recursos compartidos de red)

Las funciones de sesión de administración de red controlan las sesiones de red establecidas entre estaciones de trabajo y servidores. Las funciones requieren que el servicio de servidor se pueda iniciar en el servidor.

Las funciones de sesión se enumeran a continuación.



| Función                                       | Descripción                                                                                       |
|------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel)         | Elimina las conexiones actuales entre una estación de trabajo y un servidor; finaliza la sesión de red. |
| [**NetSessionEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netsessionenum)       | Devuelve información sobre todas las sesiones actuales establecidas para un servidor.                          |
| [**NetSessionGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiongetinfo) | Devuelve información sobre una sesión determinada.                                                   |



 

Una *sesión* es un vínculo entre una estación de trabajo y un servidor. Se establece una sesión la primera vez que una estación de trabajo realiza una conexión a un recurso compartido en el servidor. Hasta que finalice la sesión, todas las conexiones lejos entre la estación de trabajo y el servidor forman parte de la misma sesión. Para finalizar una sesión, una aplicación en el extremo del servidor de una conexión llama a la [**función NetSessionDel.**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel)

Las funciones de sesión de administración de red administran la información por usuario con el parámetro *username.* Dado que puede haber varios usuarios por sesión, este parámetro es necesario para tener acceso a la información específica del usuario para la sesión.

Las funciones de sesión están disponibles en cinco niveles de información:

<dl>

[**INFORMACIÓN \_ DE SESIÓN \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_0)  
[**INFORMACIÓN \_ DE SESIÓN \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_1)  
[**INFORMACIÓN \_ DE SESIÓN \_ 2**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_2)  
[**INFORMACIÓN \_ DE SESIÓN \_ 10**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_10)  
[**INFORMACIÓN \_ DE SESIÓN \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_502)  
</dl>

Si está programando para Active Directory, es posible que pueda llamar a determinados métodos de la interfaz de servicio (ADSI) de Active Directory para lograr la misma funcionalidad que puede lograr llamando a las funciones de sesión de administración de red. Para obtener más información, [**vea IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).

 

 
