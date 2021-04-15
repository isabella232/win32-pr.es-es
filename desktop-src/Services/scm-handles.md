---
description: El SCM es compatible con los tipos de controladores para permitir el acceso a los siguientes objetos.
ms.assetid: 5ffdd1a9-1a66-4fc4-b35d-4f744bae4897
title: Identificadores de SCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8a84fb09dbc95f3e1b5f5cee432de616f5ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669722"
---
# <a name="scm-handles"></a>Identificadores de SCM

El SCM es compatible con los tipos de controladores para permitir el acceso a los siguientes objetos.

-   La base de datos de servicios instalados.
-   Un servicio de.
-   Bloqueo de la base de datos.

Un objeto SCManager representa la base de datos de servicios instalados. Es un objeto contenedor que contiene objetos de servicio. La función [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) devuelve un identificador a un objeto SCManager en un equipo especificado. Este identificador se usa al instalar, eliminar, abrir y enumerar servicios y al bloquear la base de datos de servicios.

Un objeto de servicio representa un servicio instalado. Las funciones [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) y [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) devuelven los identificadores de los servicios instalados.

Las funciones [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera), [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)y [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) pueden solicitar distintos tipos de acceso a los objetos de servicio y SCManager. El acceso solicitado se concede o se deniega según el token de acceso del proceso de llamada y el descriptor de seguridad asociado al objeto SCManager o Service.

La función [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) cierra los identificadores de SCManager y los objetos de servicio. Cuando ya no necesite estos identificadores, asegúrese de cerrarlos.

 

 



