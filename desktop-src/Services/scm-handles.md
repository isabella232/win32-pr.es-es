---
description: El SCM admite tipos de identificador para permitir el acceso a los objetos siguientes.
ms.assetid: 5ffdd1a9-1a66-4fc4-b35d-4f744bae4897
title: Identificadores de SCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6830063e57b2135c32bf01b4fdc0b4cf6207de32198d9f88d97667f4b403fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889193"
---
# <a name="scm-handles"></a>Identificadores de SCM

El SCM admite tipos de identificador para permitir el acceso a los objetos siguientes.

-   Base de datos de servicios instalados.
-   Un servicio.
-   Bloqueo de base de datos.

Un objeto SCManager representa la base de datos de los servicios instalados. Es un objeto contenedor que contiene objetos de servicio. La [**función OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) devuelve un identificador a un objeto SCManager en un equipo especificado. Este identificador se usa al instalar, eliminar, abrir y enumerar servicios y al bloquear la base de datos de servicios.

Un objeto de servicio representa un servicio instalado. Las [**funciones CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) y [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) devuelven identificadores a los servicios instalados.

Las [**funciones OpenSCManager,**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)y [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) pueden solicitar distintos tipos de acceso a SCManager y objetos de servicio. El acceso solicitado se concede o deniega en función del token de acceso del proceso de llamada y del descriptor de seguridad asociado al SCManager o al objeto de servicio.

La [**función CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) cierra los identificadores a SCManager y a los objetos de servicio. Cuando ya no necesite estos identificadores, asegúrese de cerrarlos.

 

 



