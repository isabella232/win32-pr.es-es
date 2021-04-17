---
title: Espacio de configuración del dispositivo
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 598299c3-159f-4cad-b6a5-d282cd5bb4a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120e12b6480675dba6e735390f4820a8782edc5c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105697990"
---
# <a name="device-configuration-space-and-device-configurations"></a>Configuraciones de dispositivo y espacio de configuración de dispositivos

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El espacio de *configuración* de un dispositivo es el conjunto de todos los valores posibles que se pueden asignar a todos los atributos del dispositivo. Las dos razones más importantes para describir el espacio de configuración del dispositivo en PrintCapabilities son las siguientes.

1.  La información contribuye significativamente a un mayor conocimiento de las capacidades del dispositivo. Esta información facilita a un cliente de la PrintCapabilities la generación de elementos de la interfaz de usuario, lo que facilita que el usuario final Seleccione una configuración concreta para procesar un trabajo. Al proporcionar más detalles de las capacidades del dispositivo a la aplicación y, en última instancia, al usuario final, el intento de impresión del usuario se puede cumplir de forma más eficaz.

2.  Ciertas propiedades de dispositivo presentadas en PrintCapabilities pueden depender de la configuración concreta seleccionada por el cliente.

Parte de la información no debe incorporarse a la PrintCapabilities. Esto incluye información que no afecta al modo en que se crea un trabajo, no impone restricciones en la forma en que se crea un trabajo ni afecta a las propiedades del dispositivo. Por ejemplo, es posible que un dispositivo pueda notificar información de estado, como el conjunto de trabajos en espera de ser procesados. Esta información no tiene ningún efecto en la información necesaria para dar formato al trabajo, ni proporciona ninguna indicación de las capacidades disponibles en el dispositivo. Por esta razón, no es necesario que este tipo de información esté presente en PrintCapabilities.

## <a name="device-constraints"></a>Restricciones de dispositivos

Muchos dispositivos no admiten todas las configuraciones posibles en el espacio de configuración debido a una restricción en el dispositivo. Por ejemplo, se puede restringir un dispositivo para que no realice la impresión dúplex en un medio transparente. Una restricción puede representar una limitación física: algunos tipos de medios son simplemente demasiado rígidos para viajar a través de determinadas rutas de papel del dispositivo, por lo que no se pueden colocar en algunas ranuras de entrada ni enrutar a algunas ubicaciones de salida. Actualmente, es responsabilidad del proveedor de PrintCapabilities o PrintTicket validar la configuración representada por el PrintTicket de entrada para comprobar que no representa una configuración no válida. Si la configuración no es válida, el proveedor de PrintCapabilities o PrintTicket debe modificar la configuración de manera que sea válida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



