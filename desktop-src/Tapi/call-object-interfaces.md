---
description: El objeto Call se crea cuando llega una llamada. Las interfaces asociadas obtienen y establecen información relacionada con la llamada.
ms.assetid: cff131c0-9f4a-418d-b486-155bd71e9316
title: Llamar a interfaces de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ccb7fb9ed07fad8bd952aff806d39aa2db5e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002064"
---
# <a name="call-object-interfaces"></a>Llamar a interfaces de objeto

El [objeto Call](call-object.md) se crea cuando llega una llamada. Las interfaces asociadas obtienen y establecen información relacionada con la llamada.

Los enumeradores y las interfaces de eventos no se exponen directamente en el objeto de llamada, pero se enumeran aquí para mayor comodidad de referencia.

Las interfaces [**ITCallNotificationEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent), [**ITCallInfoChangeEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent), [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent), [**ITCallMediaEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent)y [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass) no se exponen directamente en el objeto de llamada, pero están estrechamente relacionadas con ella y se enumeran aquí para mayor comodidad de referencia.



| Interfaz                                                      | Descripción                                                                                                                  |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)                               | Proporciona información relativa a un objeto de llamada, como el estado de la llamada o los terminales en uso.                                       |
| [**ITCallInfo2**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo2)                             | Extiende [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) proporcionando métodos para establecer el filtrado de eventos en cada llamada.                    |
| [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)               | Se utiliza para conectar, responder y realizar operaciones básicas de telefonía en un objeto de llamada.                                            |
| [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2)             | Extiende [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) proporcionando métodos para seleccionar un terminal en una llamada.              |
| [**ITCallNotificationEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)     | Interfaz de notificación para [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).                                                                 |
| [**ITCallInfoChangeEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent)         | Interfaz de notificación para los cambios en la información de llamada.                                                                      |
| [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent)                   | Obtiene información sobre un evento de llamada.                                                                                    |
| [**ITCallMediaEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent)                   | Obtiene información sobre un evento de multimedia de llamada.                                                                              |
| [**ITCustomTone**](/windows/desktop/api/Tapi3if/nn-tapi3if-itcustomtone)                           | Proporciona métodos para controlar los tonos personalizados posibles con algunos conjuntos de teléfonos.                                                  |
| [**ITDetectTone**](/windows/desktop/api/Tapi3if/nn-tapi3if-itdetecttone)                           | Proporciona métodos para especificar los tonos y las características de tono que generan eventos de tono.                                    |
| [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol)   | Es compatible con aplicaciones heredadas que se deben comunicar directamente con un dispositivo.                                                   |
| [**ITLegacyCallMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacycallmediacontrol2) | Extiende [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol) proporcionando métodos de detección de tono y generación. |
| [**IEnumCall**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcall)                                 | Enumera [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).                                                                                 |



 

 

 



