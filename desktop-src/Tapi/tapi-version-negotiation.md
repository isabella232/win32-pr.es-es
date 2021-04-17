---
description: Con el tiempo, pueden existir diferentes versiones para TAPI, aplicaciones y proveedores de servicios para una línea o un teléfono.
ms.assetid: 36a17ae8-31db-4db9-a401-097d47aa26ad
title: Negociación de la versión de TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f41f4ca6f12862d6fc19f982c48b90bdafe2aaa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678167"
---
# <a name="tapi-version-negotiation"></a>Negociación de la versión de TAPI

Con el tiempo, pueden existir diferentes versiones para TAPI, aplicaciones y proveedores de servicios para una línea o un teléfono. Las nuevas versiones pueden definir nuevas características, nuevos campos para estructuras de datos, etc. Por lo tanto, los números de versión indican cómo interpretar varias estructuras de datos.

Para permitir una interoperabilidad óptima de las distintas versiones de aplicaciones, versiones de TAPI y versiones de proveedores de servicios de diferentes proveedores, TAPI proporciona un mecanismo de negociación de versión simple de dos pasos para las aplicaciones. La aplicación, TAPI y el proveedor de servicios de cada dispositivo de línea deben acordar dos versiones diferentes. El primero es el número de versión de la telefonía básica y complementaria, y se conoce como la versión de la API. El otro es para las extensiones específicas del proveedor, si existen, y se conoce como la versión de la extensión. El formato de las estructuras de datos y los tipos de datos que usan las características básicas y complementarias de TAPI se define mediante la versión de la API, mientras que la versión de la extensión determina el formato de las estructuras de datos definidas por las extensiones específicas del proveedor.

La negociación de la versión continúa en dos fases. En la primera fase, se negocia el número de versión de la API y se obtiene el identificador de extensión asociado a las extensiones específicas del proveedor admitidas en el dispositivo. En la segunda fase, se negocia la versión de la extensión. Si la aplicación no usa extensiones de API, omite la segunda fase y las extensiones no están activadas por el proveedor de servicios. Si la aplicación desea usar extensiones, pero la aplicación no reconoce las extensiones del proveedor de servicios (el identificador de extensión), la aplicación debe omitir también la negociación de la versión de la extensión. Cada proveedor tiene su propio conjunto de versiones válidas (reconocidas) para cada conjunto de especificaciones de extensión que distribuye.

La función [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) se usa para negociar el número de versión de la API que se va a usar. También recupera el identificador de extensión admitido por el dispositivo de línea y devuelve ceros si no se admiten extensiones. Con esta llamada de función, la aplicación proporciona el intervalo de versiones de API con el que es compatible. A su vez, TAPI negocia con el proveedor de servicios de la línea para determinar el intervalo de versión de la API que admite. A continuación, TAPI selecciona un número de versión (normalmente, aunque no necesariamente, el número de versión más alto) en el intervalo de versiones superpuestos que ha proporcionado la aplicación, el archivo DLL y el proveedor de servicios. Este número se devuelve a la aplicación, junto con el identificador de extensión que define las extensiones disponibles en el proveedor de servicios de esa línea.

Si la aplicación desea usar las extensiones definidas por el identificador de extensión devuelto, primero debe llamar a [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) para negociar la versión de la extensión. En una fase de negociación similar, la aplicación especifica la versión de API ya acordada y el intervalo de versiones de la extensión que admite. TAPI pasa esta información al proveedor de servicios para la línea. El proveedor de servicios comprueba la versión de la API y el intervalo de versiones de la extensión con respecto a su propio y selecciona el número de versión de la extensión adecuado, si existe.

Cuando la aplicación llama posteriormente a [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps), devuelve un conjunto de funcionalidades de dispositivo para la línea que corresponde a los resultados de la negociación de la versión. Incluyen las funcionalidades de dispositivo de la línea coherentes con la versión de la API y las capacidades específicas del dispositivo de la línea coherentes con la versión de la extensión. La aplicación debe especificar ambos números de versión cuando abre una línea. En ese momento, la aplicación, el archivo DLL y el proveedor de servicios se confirman con las versiones acordadas. Si no se van a usar extensiones específicas del dispositivo, la versión de la extensión debe especificarse como cero.

En un entorno en el que varias aplicaciones abran el mismo dispositivo de línea, la primera aplicación que abra el dispositivo de línea selecciona las versiones de todas las aplicaciones futuras que deseen usar la línea (los proveedores de servicios no admiten varias versiones simultáneamente). Del mismo modo, una aplicación que abra varios dispositivos de línea puede encontrar más fácil el funcionamiento de todos los dispositivos de línea con el mismo número de versión de la API.

Cada función que toma un parámetro *dwAPIVersion* o similar debe establecer este parámetro en la versión de API más alta admitida por la aplicación o en la versión de API negociada mediante la función [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) o [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) en un dispositivo determinado. Use la siguiente tabla como guía:



| Función                                                     | Significado                                                                               |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)             | Use la versión devuelta por [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion).   |
| [**lineGetCountry**](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)                     | Use la versión más reciente admitida por la aplicación.                                     |
| [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)                     | Use la versión devuelta por [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion).   |
| [**lineGetProviderList**](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist)           | Use la versión más reciente admitida por la aplicación.                                     |
| [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)         | Use la versión más reciente admitida por la aplicación.                                     |
| [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)   | Use la versión más reciente admitida por la aplicación.                                     |
| [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion)   | Use la versión devuelta por [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion).   |
| [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)                                 | Use la versión devuelta por [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion).   |
| [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)         | Use la versión más reciente admitida por la aplicación.                                     |
| [**lineTranslateDialog**](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog)           | Use la versión más reciente admitida por la aplicación.                                     |
| [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)                   | Use la versión devuelta por [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion). |
| [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | Use la versión más reciente admitida por la aplicación.                                     |
| [**phoneNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | Use la versión devuelta por [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion). |
| [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)                               | Use la versión devuelta por [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion). |



 

> [!IMPORTANT]
> Al negociar una versión de API, establezca siempre los números de versión alta y baja en el intervalo de versiones que pueda admitir la aplicación. Por ejemplo, nunca use 0x00000000 para la versión baja o 0xFFFFFFFF para el alto, ya que estos valores requieren que la aplicación admita todas las versiones de TAPI, tanto en el pasado como en el futuro.

 

 

 



