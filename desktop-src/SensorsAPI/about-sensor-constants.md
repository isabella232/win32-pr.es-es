---
description: Acerca de las constantes de sensor
ms.assetid: ba85ccd8-5251-4e47-84da-80899fe84c39
title: Acerca de las constantes de sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea862d38af74058d11d3a6fa1eb11a702b3b277
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546523"
---
# <a name="about-sensor-constants"></a>Acerca de las constantes de sensor

El sensor de Windows y la plataforma de ubicación usan constantes de muchas maneras. La plataforma define diferentes constantes que puede usar en el código del controlador del sensor. Los fabricantes de sensores pueden definir constantes personalizadas. Puede encontrar las definiciones de las constantes definidas por la plataforma en el archivo Sensors. h. Para obtener información detallada sobre las constantes de sensor definidas por la plataforma, vea [constantes](constants.md).

### <a name="sensor-and-data-organization"></a>Sensor y organización de datos

La plataforma organiza los sensores y los datos de las siguientes maneras.

-   Las categorías representan amplias clases de dispositivos de sensor. Las categorías permiten agrupar sensores que es probable que proporcionen tipos similares de información o que, de otro modo, estén relacionados de alguna manera. Cada categoría se representa mediante una constante **GUID** . Por ejemplo, los sensores que notifican las coordenadas de latitud y longitud pertenecen a la categoría de sensor de ubicación. Esto se representented por la constante de ubicación de categoría de SENSOR \_ \_ .
-   Los tipos de sensor representan tipos específicos de sensores. Cada tipo de sensor encaja en una categoría determinada. Dos sensores de distintos tipos pueden pertenecer a la misma categoría o a distintas categorías. Cada tipo de sensor se representa mediante una constante **GUID** . Por ejemplo, un sensor del sistema de posicionamiento global se identificaría mediante \_ la \_ constante de GPS ubicación de tipo de sensor \_ . Sin embargo, un sensor que proporciona la ubicación actual mediante una dirección IP se identificaría mediante la constante de búsqueda de ubicación del tipo de SENSOR \_ \_ \_ . Sin embargo, ambos sensores pertenecierían a la categoría sensor de ubicación.
-   Los tipos de datos representan tipos específicos de información que el sensor puede proporcionar. Los tipos de datos del sensor pueden contener el valor de medida real, como altitud; información acerca de las unidades utilizadas para expresar los datos, como los medidores; y los puntos de referencia de los datos, como el nivel del mar. Cada tipo de datos se representa mediante una constante **PROPERTYKEY** . Por ejemplo, el tipo de datos que representa la altitud sobre el nivel del mar, en metros, se identificaría mediante la constante de tipo de datos de SENSOR \_ \_ \_ altitud \_ SEALEVEL \_ metros.
-   Cuando se informa de los datos, se dice que un valor está incluido en un campo de datos y una colección de campos de datos relacionados constituye un informe de datos. Los informes de datos se empaquetan juntos mediante la interfaz [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) . Cada informe de datos debe contener al menos un campo de datos válido y una marca de tiempo que identifique Cuándo se creó el informe de datos. Las marcas de tiempo se representan mediante la \_ constante timestamp del tipo de datos del sensor \_ \_ .

### <a name="other-constants"></a>Otras constantes

El programa debe usar también otras constantes. Entre estas constantes se incluyen las siguientes:

-   Propiedades del sensor, como la descripción de la propiedad del SENSOR \_ \_ . Normalmente, estas constantes se utilizan para describir un sensor. El sensor debe proporcionar algunas propiedades de sensor, las aplicaciones cliente pueden establecer algunas propiedades y algunas siempre deben devolver el mismo valor del sensor. La sección de referencia de [**las propiedades del sensor**](sensor-properties.md) proporciona esta información para cada propiedad.
-   Constantes de evento, como el estado de evento de SENSOR \_ \_ \_ cambiado. Las constantes de evento incluyen **GUID** s, que representan tipos de eventos, y **PROPERTYKEY** s, que representan los tipos de parámetros de evento. Usará estas constantes para las llamadas a métodos, como [**ISensor:: SetEventInterest**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventinterest) y [**ISensor:: GetEventInterest**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-geteventinterest).

### <a name="custom-constants"></a>Constantes personalizadas

Los fabricantes de sensores pueden definir constantes personalizadas. Por ejemplo, un sensor puede pertenecer a una categoría no definida por la plataforma. Para poder usar un sensor que defina constantes personalizadas, el fabricante del sensor debe publicar los valores, por ejemplo, mediante la publicación de un archivo de encabezado. Para obtener más información, consulte la documentación que se proporciona con el sensor.

 

 
