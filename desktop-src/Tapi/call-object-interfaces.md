---
description: El objeto Call se crea cuando existe una llamada. Las interfaces asociadas obtienen y establecen información relacionada con la llamada.
ms.assetid: cff131c0-9f4a-418d-b486-155bd71e9316
title: Llamar a interfaces de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41d01c95ff2f387345eae570ef3cc67012e826a9ee104161d9c4a279118c121
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117947703"
---
# <a name="call-object-interfaces"></a>Llamar a interfaces de objeto

El [objeto Call](call-object.md) se crea cuando existe una llamada. Las interfaces asociadas obtienen y establecen información relacionada con la llamada.

Las interfaces de enumeradores y eventos no se exponen directamente en el objeto call, pero se enumeran aquí para mayor comodidad de referencia.

Las interfaces [**ITCallNotificationEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent), [**ITCallInfoChangeEvent,**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent) [**ITCallStateEvent,**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent) [**ITCallMediaEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent)e [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass) no se exponen directamente en el objeto Call, pero están estrechamente relacionadas con él y se enumeran aquí para mayor comodidad de referencia.



| Interfaz                                                      | Descripción                                                                                                                  |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)                               | Proporciona información sobre un objeto Call, como el estado de la llamada o los terminales en uso.                                       |
| [**ITCallInfo2**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo2)                             | Extiende [**ITCallInfo proporcionando métodos**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) para establecer el filtrado de eventos por llamada.                    |
| [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)               | Se usa para conectarse, responder y realizar operaciones básicas de telefonía en un objeto de llamada.                                            |
| [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2)             | Extiende [**ITBasicCallControl proporcionando**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) métodos para seleccionar un terminal en una llamada.              |
| [**ITCallNotificationEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)     | Interfaz de notificación [**para ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).                                                                 |
| [**ITCallInfoChangeEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent)         | Interfaz de notificación para los cambios en la información de llamada.                                                                      |
| [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent)                   | Obtiene información sobre un evento de llamada.                                                                                    |
| [**ITCallMediaEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent)                   | Obtiene información sobre un evento multimedia de llamada.                                                                              |
| [**ITCustomTone**](/windows/desktop/api/Tapi3if/nn-tapi3if-itcustomtone)                           | Proporciona métodos para controlar los tonos personalizados posibles con algunos conjuntos de teléfonos.                                                  |
| [**ITDetectTone**](/windows/desktop/api/Tapi3if/nn-tapi3if-itdetecttone)                           | Proporciona métodos para especificar los tonos y las características del tono que generan eventos de tono.                                    |
| [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol)   | Admite aplicaciones heredadas que deben comunicarse directamente con un dispositivo.                                                   |
| [**ITLegacyCallMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacycallmediacontrol2) | Extiende [**ITLegacyCallMediaControl proporcionando**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol) métodos para la detección y generación de tono. |
| [**IEnumCall**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcall)                                 | Enumera [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).                                                                                 |



 

 

 



