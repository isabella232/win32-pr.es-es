---
title: Espacio de configuración del dispositivo
description: El espacio de configuración de un dispositivo es el conjunto de todos los valores posibles que se pueden asignar a todos los atributos del dispositivo.
ms.assetid: 598299c3-159f-4cad-b6a5-d282cd5bb4a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e09eabf7c84e1990e0aaf6b2d9fab1d9043f788fef32c3863a71d9ca1e6b61a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092125"
---
# <a name="device-configuration-space-and-device-configurations"></a>Espacio de configuración del dispositivo y configuraciones de dispositivos

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El espacio de configuración *de un dispositivo* es el conjunto de todos los valores posibles que se pueden asignar a todos los atributos del dispositivo. Las dos razones más importantes para describir el espacio de configuración del dispositivo en PrintCapabilities son las siguientes.

1.  La información contribuye significativamente a un mayor conocimiento de las funcionalidades del dispositivo. Esta información facilita que un cliente de PrintCapabilities genere elementos de interfaz de usuario (UI), lo que facilita al usuario final seleccionar una configuración determinada para procesar un trabajo. Al proporcionar más detalles de las funcionalidades del dispositivo a la aplicación y, en última instancia, al usuario final, la intención de impresión del usuario se puede cumplir de forma más eficaz.

2.  Algunas propiedades de dispositivo que se presentan en PrintCapabilities pueden depender de la configuración determinada seleccionada por el cliente.

No se debe incorporar información a PrintCapabilities. Esto incluye información que no afecta a la forma en que se crea un trabajo, no impone restricciones en la forma en que se crea un trabajo ni afecta de otro modo a las propiedades del dispositivo. Por ejemplo, un dispositivo podría ser capaz de notificar información de estado, como el conjunto de trabajos que esperan a ser procesados. Esta información no tiene ningún efecto en la información necesaria para dar formato al trabajo, ni proporciona ninguna indicación de las funcionalidades disponibles en el dispositivo. Por este motivo, no es necesario que este tipo de información esté presente en PrintCapabilities.

## <a name="device-constraints"></a>Restricciones de dispositivo

Muchos dispositivos no admiten todas las configuraciones posibles en el espacio de configuración debido a una restricción en el dispositivo. Por ejemplo, se puede restringir a un dispositivo la realización de la impresión dúplex en medios transparentes. Una restricción puede representar una limitación física: algunos tipos de medios simplemente son demasiado rígidos para desplazarse por determinadas rutas de acceso de papel en el dispositivo, por lo que no se pueden colocar en algunas ranuras de entrada ni enrutar a algunos cubos de salida. Actualmente es responsabilidad del proveedor PrintCapabilities o PrintTicket validar la configuración representada por la entrada PrintTicket, para comprobar que no representa una configuración no válida. Si la configuración no es válida, el proveedor PrintCapabilities o PrintTicket debe modificar la configuración de forma que sea válida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



