---
description: El Teléfono es la entidad que representa el dispositivo telefónico real y todos sus controles.
ms.assetid: 5bc2f595-8e2b-4938-b813-1574a9390084
title: Teléfono Interfaces de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f39b163e895a512e7adc7be5c2fb848c5849361
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071085"
---
# <a name="phone-object-interfaces"></a>Teléfono Interfaces de objetos

El Teléfono es la entidad que representa el dispositivo telefónico real y todos sus controles.

Las interfaces [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) e [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) no se exponen directamente en el objeto Teléfono, pero están estrechamente relacionadas con él y se enumeran aquí por comodidad de referencia.



| Interfaz                                                  | Descripción                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                 | Permite el acceso al dispositivo de teléfono en un nivel comparable al disponible con TAPI 2. *x* API de C.                                      |
| [**ITAutomatedPhoneControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) | Proporciona métodos para el control automatizado de los tonos y anillos de un teléfono, y para el control de llamadas automatizado en función del estado del conmutador de enlace de un teléfono. |
| [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)                       | Recupera la descripción de los eventos de teléfono.                                                                                                |
| [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                           | Enumera [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone).                                                                                                    |



 

 

 



