---
description: La operación de estacionamiento permite a una aplicación enviar una sesión a una dirección especial en la que se conservará hasta que se haya desactivado.
ms.assetid: 6a82f03e-d8fd-4d0b-8f5d-f7934ba86759
title: Aparcamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aded4657a9d337d6d9c663622a5359856e964b90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677939"
---
# <a name="park"></a>Aparcamiento

La operación de estacionamiento permite a una aplicación enviar una sesión a una dirección especial en la que se conservará hasta que se haya desactivado. Desde el punto de vista de la aplicación, esto se parece mucho a una transferencia. Para la entidad en el otro extremo de la conexión, esto se asemeja a poner en espera.

La diferencia entre estacionamiento y transferencia es que la dirección deestacionada no es un punto de conexión para la sesión y la sesión no alerta ni agota el tiempo de espera. La diferencia entre estacionamiento y Hold es que una vez finalizada la operación de estacionamiento, la sesión ya no está asociada a la dirección de la aplicación.

Se proporcionan dos formas de estacionamiento de una sesión: estacionamiento *dirigido* y no *Redirigido*. En el parque de llamadas dirigidas, la aplicación especifica la dirección de destino en la que se va a detener la llamada. Con estacionamiento no directo, el proveedor de servicios o el hardware subyacente determinan la dirección y la devuelven a la aplicación.

Una sesión aparcada normalmente entra en el estado de inactividad después de haberse detenido correctamente y, a continuación, la aplicación debe liberar los recursos asociados a ella. Vea [finalizar una sesión](terminate-a-session-ovr.md) para obtener un resumen de cómo hacerlo.

Si la aplicación se desactivará la sesión, se asignarán nuevos recursos de la sesión, incluso si la aplicación ha devuelto los punteros anteriores, por lo que si no se realizan las versiones adecuadas, se pueden producir diversos problemas.

Algunos proveedores de servicios pueden recordar al usuario una vez que se ha detenido una sesión durante un período de tiempo prolongado. La aplicación ve una llamada de oferta con un [motivo](reason-ovr.md) de llamada establecido en recordatorio.

No todos los proveedores de servicios admiten el uso de esta operación.

**TAPI 2. x:** Vea [**linePark**](/windows/win32/api/tapi/nf-tapi-linepark), [**lineUnpark**](/windows/win32/api/tapi/nf-tapi-lineunpark).

**TAPI 3:** Vea [**ITBasicCallControl::P arkdirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect), [**ITBasicCallControl::P arkindirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect), [**ITBasicCallControl:: unpark**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark).

 

 
