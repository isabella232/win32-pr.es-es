---
description: El Teléfono es la entidad que representa el dispositivo de teléfono real y todos sus controles.
ms.assetid: 5bc2f595-8e2b-4938-b813-1574a9390084
title: Teléfono Interfaces de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e146910b8184f35057843f20ad663e2be21d2c4844852e7cca3939e1e979d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873275"
---
# <a name="phone-object-interfaces"></a>Teléfono Interfaces de objeto

El Teléfono es la entidad que representa el dispositivo de teléfono real y todos sus controles.

Las [**interfaces ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) e [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) no se exponen directamente en el objeto Teléfono, sino que están estrechamente relacionadas con él y se enumeran aquí para mayor comodidad.



| Interfaz                                                  | Descripción                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                 | Permite el acceso al dispositivo de teléfono en un nivel comparable al disponible con TAPI 2. *x* API de C.                                      |
| [**ITAutomatedPhoneControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) | Proporciona métodos para el control automatizado de los tonos y anillos de un teléfono, y para el control de llamadas automatizado en función del estado del conmutador de enlace de un teléfono. |
| [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)                       | Recupera la descripción de los eventos de teléfono.                                                                                                |
| [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                           | Enumera [**ITPhone.**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                                                                                    |



 

 

 



