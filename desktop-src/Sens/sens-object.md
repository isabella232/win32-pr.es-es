---
description: El Servicio de notificación de eventos del sistema (SENS) define la coclase de SENS como parte de la biblioteca de tipos SENS.
ms.assetid: b494808c-1116-47ac-8713-0d515b312368
title: Sens (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acdf70b5e2229051d569bd1f607ad8db5d3d567b4c0421464757f02bc6a8e4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003953"
---
# <a name="sens-object"></a>Sens (objeto)

El Servicio de notificación de eventos del sistema (SENS) define la coclase de SENS como parte de la biblioteca de tipos SENS.

## <a name="implementation"></a>Implementación

El sistema operativo proporciona la implementación del objeto SENS.

## <a name="creationaccess-functions"></a>Funciones de creación y acceso



| Función                                      | Descripción                                             |
|-----------------------------------------------|---------------------------------------------------------|
| [**Cocreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) | Crea una instancia del objeto SENS mediante su CLSID. |



 

## <a name="interfaces"></a>Interfaces



| Interfaz                            | Descripción                                                                                         |
|--------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**IsensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork) | Predeterminada. Interfaz saliente implementada por el objeto receptor en la aplicación de suscriptor.                   |
| [**IsensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)     | Interfaz saliente implementada por el objeto receptor en la aplicación de suscriptor.                            |
| [**IsensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)     | Interfaz saliente implementada por el objeto receptor en la aplicación de suscriptor.                            |
| [**IsensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2)   | Interfaz saliente implementada por el objeto receptor en la aplicación de suscriptor. Disponible con Windows XP. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)
</dt> <dt>

[**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork)
</dt> <dt>

[**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)
</dt> <dt>

[Acerca del servicio de notificación de eventos del sistema](about-system-event-notification-service.md)
</dt> </dl>

 

 
