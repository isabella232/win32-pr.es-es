---
description: Acerca de las constantes de sensor
ms.assetid: ba85ccd8-5251-4e47-84da-80899fe84c39
title: Acerca de las constantes de sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45cab8b5def4cdfa185a55dd993896fb5157563424b7753497413e5d7706465e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890260"
---
# <a name="about-sensor-constants"></a>Acerca de las constantes de sensor

La plataforma Windows sensor y ubicación utiliza constantes de muchas maneras. La plataforma define diferentes constantes que puede usar en el código del controlador del sensor. Los fabricantes de sensores pueden definir constantes personalizadas. Puede encontrar las definiciones de constantes definidas por la plataforma en el archivo Sensors.h. Para obtener información detallada sobre las constantes de sensor definidas por la plataforma, vea [Constantes](constants.md).

### <a name="sensor-and-data-organization"></a>Organización de sensores y datos

La plataforma organiza los sensores y los datos de las maneras siguientes.

-   Las categorías representan clases amplias de dispositivos de sensor. Las categorías permiten agrupar sensores que probablemente proporcionen tipos similares de información o que estén relacionados de alguna manera. Cada categoría se representa mediante una **constante GUID.** Por ejemplo, los sensores que informan de coordenadas de latitud y longitud pertenecen a la categoría del sensor de ubicación. Esto se representa mediante la constante SENSOR \_ CATEGORY \_ LOCATION.
-   Los tipos de sensor representan tipos específicos de sensores. Cada tipo de sensor se ajusta a una categoría determinada. Dos sensores de tipos diferentes pueden pertenecer a la misma categoría o categorías diferentes. Cada tipo de sensor se representa mediante una **constante GUID.** Por ejemplo, un sensor del sistema de posicionamiento global se identificaría mediante la constante SENSOR \_ TYPE \_ LOCATION \_ GPS. Sin embargo, un sensor que proporciona la ubicación actual mediante una dirección IP se identificaría mediante la constante SENSOR \_ TYPE \_ LOCATION \_ LOOKUP. Sin embargo, ambos sensores pertenecería a la categoría del sensor de ubicación.
-   Los tipos de datos representan tipos específicos de información que el sensor puede proporcionar. Los tipos de datos del sensor pueden contener el valor de medida real, como la altitud; información sobre las unidades usadas para expresar los datos, como medidores; y los puntos de referencia de los datos, como el nivel del mar. Cada tipo de datos se representa mediante una **constante PROPERTYKEY.** Por ejemplo, el tipo de datos que representa la altitud sobre el nivel del mar, en metros, se identificaría mediante la constante SENSOR \_ DATA \_ TYPE ALTITUDE \_ \_ SEALEVEL \_ METERS.
-   Al notificar datos, se dice que un valor está contenido en un campo de datos y una colección de campos de datos relacionados forma un informe de datos. Los informes de datos se empaquetan juntos mediante la [interfaz IPortableDeviceValues.](/previous-versions//ms740012(v=vs.85)) Cada informe de datos debe contener al menos un campo de datos válido y una marca de tiempo que identifique cuándo se creó el informe de datos. Las marcas de tiempo se representan mediante la constante TIMESTAMP \_ DEL TIPO DE DATOS DEL \_ \_ SENSOR.

### <a name="other-constants"></a>Otras constantes

El programa también debe usar otras constantes. Estas constantes incluyen lo siguiente:

-   Propiedades del sensor, como LA \_ DESCRIPCIÓN DE LA PROPIEDAD DEL \_ SENSOR. Normalmente, estas constantes se usan para describir un sensor. El sensor debe proporcionar algunas propiedades del sensor, algunas propiedades las pueden establecer las aplicaciones cliente y otras siempre deben devolver el mismo valor desde el sensor. La [**sección de referencia Propiedades**](sensor-properties.md) del sensor proporciona esta información para cada propiedad.
-   Constantes de evento, como SENSOR \_ EVENT \_ STATE \_ CHANGED. Las constantes de evento **incluyen GUID,** que representan tipos de eventos, y **PROPERTYKEY,** que representan tipos de parámetros de evento. Usará estas constantes para las llamadas a métodos, como [**ISensor::SetEventInterest**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventinterest) [**e ISensor::GetEventInterest.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-geteventinterest)

### <a name="custom-constants"></a>Constantes personalizadas

Los fabricantes de sensores pueden definir constantes personalizadas. Por ejemplo, un sensor puede pertenecer a una categoría no definida por la plataforma. Para poder usar un sensor que defina constantes personalizadas, el fabricante del sensor debe publicar los valores, por ejemplo, mediante la publicación de un archivo de encabezado. Para más información, consulte la documentación que se proporciona con el sensor.

 

 
