---
description: El servicio de notificación de eventos del sistema (SENS) define la coclase SENS como parte de la biblioteca de tipos SENS.
ms.assetid: b494808c-1116-47ac-8713-0d515b312368
title: SENS (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d0d5cd857063d6ac224de66610d2604db619d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668305"
---
# <a name="sens-object"></a>SENS (objeto)

El servicio de notificación de eventos del sistema (SENS) define la coclase SENS como parte de la biblioteca de tipos SENS.

## <a name="implementation"></a>Implementación

El sistema operativo proporciona la implementación del objeto SENS.

## <a name="creationaccess-functions"></a>Funciones de creación/acceso



| Función                                      | Descripción                                             |
|-----------------------------------------------|---------------------------------------------------------|
| [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) | Crea una instancia del objeto SENS utilizando su CLSID. |



 

## <a name="interfaces"></a>Interfaces



| Interfaz                            | Descripción                                                                                         |
|--------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**IsensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork) | Predeterminada. Interfaz de salida implementada por el objeto receptor en la aplicación del suscriptor.                   |
| [**IsensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)     | Interfaz de salida implementada por el objeto receptor en la aplicación del suscriptor.                            |
| [**IsensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)     | Interfaz de salida implementada por el objeto receptor en la aplicación del suscriptor.                            |
| [**IsensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2)   | Interfaz de salida implementada por el objeto receptor en la aplicación del suscriptor. Disponible con Windows XP. |



 

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

 

 
