---
description: La interfaz IUpdateService define las siguientes propiedades.
ms.assetid: 33bc28e8-0b83-4d58-a03e-ccf2a97887e6
title: Propiedades de IUpdateService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ff3cf92c89a5ba02b7d95f1a1c99f33de3202d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497602"
---
# <a name="iupdateservice-properties"></a>Propiedades de IUpdateService

La interfaz [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) define las siguientes propiedades.



| Propiedad                                                              | Descripción                                                                                     |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**CanRegisterWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_canregisterwithau)         | Obtiene un valor booleano que indica si el servicio se puede registrar con Actualizaciones automáticas.    |
| [**ContentValidationCert**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_contentvalidationcert) | Obtiene un hash SHA-1 del certificado que se utiliza para firmar el contenido del servicio.         |
| [**ExpirationDate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_expirationdate)               | Obtiene la fecha en la que el archivo. cab de autorización expira.                                  |
| [**IsManaged (**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_ismanaged)                         | Obtiene un valor booleano que indica si un servicio es un servicio administrado.                     |
| [**IsRegisteredWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isregisteredwithau)       | Obtiene un valor booleano que indica si un servicio está registrado con Actualizaciones automáticas.     |
| [**IsScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isscanpackageservice)   | Obtiene un valor booleano que indica si un servicio se basa en un paquete de examen.               |
| [**IssueDate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_issuedate)                         | Obtiene la fecha en la que se emitió el archivo. cab de autorización.                               |
| [**Name**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_name)                                   | Obtiene el nombre del servicio.                                                                   |
| [**OffersWindowsUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_offerswindowsupdates)   | Obtiene un valor booleano que indica si el servicio actual ofrece actualizaciones de actualizaciones de Windows. |
| [**RedirectUrls**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_redirecturls)                   | Obtiene la dirección URL del archivo. cab del redirector.                                                   |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceid)                         | Obtiene el identificador de un servicio.                                                              |
| [**ServiceUrl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceurl)                       | Obtiene la dirección URL para el servicio.                                                                   |
| [**SetupPrefix**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_setupprefix)                     | Obtiene el prefijo de los archivos de instalación.                                                            |



 

 

 



