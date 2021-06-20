---
title: Funciones de sesión (administración de redes)
description: Revise las funciones de sesión, que son un grupo de funciones de administración de red. Estas funciones controlan las sesiones de red establecidas entre estaciones de trabajo y servidores.
ms.assetid: ef912cd9-be5c-4202-89aa-e60f275e8938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78479391e4dc2d2aa0ced8af16a8b6cf6f3a9b05
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406128"
---
# <a name="session-functions-network-management"></a>Funciones de sesión (administración de redes)

Las funciones de sesión de administración de red controlan las sesiones de red establecidas entre estaciones de trabajo y servidores. Las funciones requieren que el servicio de servidor se pueda iniciar en el servidor.

Las funciones de sesión se enumeran a continuación.



| Función                                      | Descripción                                                                                       |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**NetSessionDel**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel)         | Elimina las conexiones actuales entre una estación de trabajo y un servidor; finaliza la sesión de red. |
| [**NetSessionEnum**](/windows/desktop/api/lmshare/nf-lmshare-netsessionenum)       | Devuelve información sobre todas las sesiones actuales establecidas para un servidor.                          |
| [**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) | Devuelve información sobre una sesión determinada.                                                   |



 

Una *sesión* es un vínculo entre una estación de trabajo y un servidor. Se establece una sesión la primera vez que una estación de trabajo realiza una conexión a un recurso compartido en el servidor. Hasta que finalice la sesión, todas las conexiones lejos entre la estación de trabajo y el servidor forman parte de la misma sesión. Para finalizar una sesión, una aplicación en el final del servidor de una conexión llama a la [**función NetSessionDel.**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel)

Las funciones de sesión de administración de red administran información por usuario con el parámetro *username.* Dado que puede haber varios usuarios por sesión, este parámetro es necesario para tener acceso a la información específica del usuario para la sesión.

Las funciones de sesión están disponibles en los siguientes niveles de información:

-   [**INFORMACIÓN \_ DE SESIÓN \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-session_info_0)
-   [**INFORMACIÓN \_ DE SESIÓN \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-session_info_1)
-   [**INFORMACIÓN \_ DE SESIÓN \_ 2**](/windows/desktop/api/lmshare/ns-lmshare-session_info_2)
-   [**INFORMACIÓN \_ DE SESIÓN \_ 10**](/windows/desktop/api/lmshare/ns-lmshare-session_info_10)
-   [**INFORMACIÓN \_ DE SESIÓN \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-session_info_502)

Si está programando para Active Directory, puede llamar a determinados métodos de la interfaz de servicio (ADSI) de Active Directory para lograr la misma funcionalidad que puede lograr mediante una llamada a las funciones de sesión de administración de red. Para obtener más información, [**vea IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).

 

 
