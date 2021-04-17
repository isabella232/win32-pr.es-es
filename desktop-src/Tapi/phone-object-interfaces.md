---
description: El objeto Phone es la entidad que representa el dispositivo de teléfono real y todos sus controles.
ms.assetid: 5bc2f595-8e2b-4938-b813-1574a9390084
title: Interfaces de objetos de teléfono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f39b163e895a512e7adc7be5c2fb848c5849361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688003"
---
# <a name="phone-object-interfaces"></a>Interfaces de objetos de teléfono

El objeto Phone es la entidad que representa el dispositivo de teléfono real y todos sus controles.

Las interfaces [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) y [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) no se exponen directamente en el objeto Phone, sino que están estrechamente relacionadas con ella y se enumeran aquí para facilitar la referencia.



| Interfaz                                                  | Descripción                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                 | Permite el acceso al dispositivo telefónico en un nivel comparable al disponible en TAPI 2. *x* C API.                                      |
| [**ITAutomatedPhoneControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) | Proporciona métodos para el control automatizado de tonos y anillos de un teléfono, y para el control automático de llamadas basado en el estado de conmutador de un teléfono. |
| [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)                       | Recupera la descripción de los eventos de teléfono.                                                                                                |
| [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                           | Enumera [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone).                                                                                                    |



 

 

 



