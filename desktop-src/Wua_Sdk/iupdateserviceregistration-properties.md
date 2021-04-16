---
description: La interfaz IUpdateServiceRegistration define las siguientes propiedades.
ms.assetid: 2bcde8b4-7bff-4887-8080-89da817afb5f
title: Propiedades de IUpdateServiceRegistration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716c06f2fc8ed9a7ce12542a09440cf0ec0b5c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696244"
---
# <a name="iupdateserviceregistration-properties"></a>Propiedades de IUpdateServiceRegistration

La interfaz **IUpdateServiceRegistration** define las siguientes propiedades.



| Propiedad                                                                                      | Descripción                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsPendingRegistrationWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_ispendingregistrationwithau) | Obtiene un valor booleano que indica si el servicio también se registrará con Actualizaciones automáticas, cuando se agregue.                                  |
| [**RegistrationState**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_registrationstate)                     | Obtiene un valor [**UpdateServiceRegistrationState**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) que indica el estado actual del registro del servicio. |
| [**Servicio**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_service)                                         | Obtiene un puntero a una interfaz [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) . Esta propiedad es la propiedad predeterminada.                                    |



 

 

 



