---
title: Funciones de sesión (administración de red)
description: Las funciones de sesión de administración de red controlan las sesiones de red establecidas entre estaciones de trabajo y servidores. Las funciones requieren que se inicie el servicio servidor en el servidor.
ms.assetid: ef912cd9-be5c-4202-89aa-e60f275e8938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b1e0236881b50f0363a6c872394cfe42f44748
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103904954"
---
# <a name="session-functions-network-management"></a>Funciones de sesión (administración de red)

Las funciones de sesión de administración de red controlan las sesiones de red establecidas entre estaciones de trabajo y servidores. Las funciones requieren que se inicie el servicio servidor en el servidor.

A continuación se enumeran las funciones de sesión.



| Función                                      | Descripción                                                                                       |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**NetSessionDel**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel)         | Elimina las conexiones actuales entre una estación de trabajo y un servidor. finaliza la sesión de red. |
| [**NetSessionEnum**](/windows/desktop/api/lmshare/nf-lmshare-netsessionenum)       | Devuelve información acerca de todas las sesiones actuales establecidas para un servidor.                          |
| [**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) | Devuelve información sobre una sesión determinada.                                                   |



 

Una *sesión* es un vínculo entre una estación de trabajo y un servidor. Una sesión se establece la primera vez que una estación de trabajo realiza una conexión a un recurso compartido en el servidor. Hasta que finalice la sesión, todas las conexiones posteriores entre la estación de trabajo y el servidor formarán parte de la misma sesión. Para finalizar una sesión, una aplicación en el extremo del servidor de una conexión llama a la función [**NetSessionDel**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel) .

Las funciones de sesión de administración de red administran la información por usuario con el parámetro de *nombre de usuario* . Dado que puede haber varios usuarios por sesión, este parámetro es necesario para tener acceso a la información específica del usuario para la sesión.

Las funciones de sesión están disponibles en los siguientes niveles de información:

-   [**Información de sesión \_ \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-session_info_0)
-   [**Información de sesión \_ \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-session_info_1)
-   [**Información de sesión \_ \_ 2**](/windows/desktop/api/lmshare/ns-lmshare-session_info_2)
-   [**Información de la sesión \_ \_ 10**](/windows/desktop/api/lmshare/ns-lmshare-session_info_10)
-   [**Información de sesión \_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-session_info_502)

Si programa para Active Directory, es posible que pueda llamar a determinados métodos de la interfaz de servicio Active Directory (ADSI) para lograr la misma funcionalidad que puede lograr mediante una llamada a las funciones de sesión de administración de red. Para obtener más información, vea [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) y [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).

 

 
