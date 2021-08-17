---
description: Con el tiempo, pueden existir versiones diferentes para TAPI, aplicaciones y proveedores de servicios para una línea o teléfono.
ms.assetid: 36a17ae8-31db-4db9-a401-097d47aa26ad
title: Negociación de versiones de TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cd6d816c07cb1c6c93d9cc219509f257d9a2695671b5197002171f0f819f17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404070"
---
# <a name="tapi-version-negotiation"></a>Negociación de versiones de TAPI

Con el tiempo, pueden existir versiones diferentes para TAPI, aplicaciones y proveedores de servicios para una línea o teléfono. Las nuevas versiones pueden definir nuevas características, nuevos campos para estructuras de datos, y así sucesivamente. Por lo tanto, los números de versión indican cómo interpretar varias estructuras de datos.

Para permitir una interoperabilidad óptima de diferentes versiones de aplicaciones, versiones de TAPI propiamente dichas y versiones de proveedores de servicios por parte de distintos proveedores, TAPI proporciona un mecanismo sencillo de negociación de versiones en dos pasos para las aplicaciones. La aplicación, TAPI y el proveedor de servicios deben acordar dos versiones diferentes para cada dispositivo de línea. El primero es el número de versión de telefonía básica y complementaria y se conoce como versión de API. El otro es para extensiones específicas del proveedor, si las hay, y se conoce como la versión de extensión. El formato de las estructuras de datos y los tipos de datos utilizados por las características básicas y adicionales de TAPI se define mediante la versión de API, mientras que la versión de extensión determina el formato de las estructuras de datos definidas por las extensiones específicas del proveedor.

La negociación de versiones continúa en dos fases. En la primera fase, se negocia el número de versión de la API y se obtiene el identificador de extensión asociado a las extensiones específicas del proveedor admitidas en el dispositivo. En la segunda fase, se negocia la versión de la extensión. Si la aplicación no usa ninguna extensión de API, omite la segunda fase y el proveedor de servicios no activa las extensiones. Si la aplicación quiere usar extensiones, pero la aplicación no reconoce las extensiones del proveedor de servicios (el identificador de extensión), la aplicación también debe omitir la negociación de la versión de la extensión. Cada proveedor tiene su propio conjunto de versiones legales (reconocidas) para cada conjunto de especificaciones de extensión que distribuye.

La [**función lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) se usa para negociar el número de versión de API que se va a usar. También recupera el identificador de extensión admitido por el dispositivo de línea y devuelve ceros si no se admite ninguna extensión. Con esta llamada de función, la aplicación proporciona el intervalo de versiones de API con el que es compatible. TAPI a su vez negocia con el proveedor de servicios de la línea para determinar qué intervalo de versiones de API admite. A continuación, TAPI selecciona un número de versión (normalmente, aunque no necesariamente el número de versión más alto) en el intervalo de versiones superpuesto que la aplicación, el archivo DLL y el proveedor de servicios han proporcionado. Este número se devuelve a la aplicación, junto con el identificador de extensión que define las extensiones disponibles en el proveedor de servicios de esa línea.

Si la aplicación quiere usar las extensiones definidas por el identificador de extensión devuelto, primero debe llamar a [**lineNegotiateExtVersion para**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) negociar la versión de la extensión. En una fase de negociación similar, la aplicación especifica la versión de API ya acordado y el intervalo de versiones de extensión que admite. TAPI pasa esta información al proveedor de servicios para la línea. El proveedor de servicios comprueba la versión de la API y el intervalo de versiones de la extensión con respecto a la suya propia, y selecciona el número de versión de extensión adecuado, si existe uno.

Cuando la aplicación llama posteriormente a [**lineGetDevCaps,**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)devuelve un conjunto de funcionalidades de dispositivo para la línea que corresponden a los resultados de la negociación de versiones. Entre ellas se incluyen las funcionalidades del dispositivo de la línea coherentes con la versión de API y las funcionalidades específicas del dispositivo de la línea coherentes con la versión de la extensión. La aplicación debe especificar ambos números de versión cuando abre una línea. En ese momento, la aplicación, el archivo DLL y el proveedor de servicios se comprometen a usar las versiones acordados. Si no se van a usar extensiones específicas del dispositivo, la versión de la extensión debe especificarse como cero.

En un entorno donde varias aplicaciones abren el mismo dispositivo de línea, la primera aplicación que abre el dispositivo de línea selecciona las versiones de todas las aplicaciones futuras que desean usar la línea (los proveedores de servicios no admiten varias versiones simultáneamente). De forma similar, una aplicación que abre varios dispositivos de línea puede resultar más fácil operar todos los dispositivos de línea con el mismo número de versión de API.

Cada función que toma *un parámetro dwAPIVersion* o similar debe establecer este parámetro en la versión de API más alta admitida por la aplicación o en la versión de API negociada mediante la función [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) o [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) en un dispositivo determinado. Use la siguiente tabla como guía:



| Función                                                     | Significado                                                                               |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)             | Use la versión devuelta [**por lineNegotiateAPIVersion.**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)   |
| [**lineGetCountry**](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)                     | Use la versión más alta compatible con la aplicación.                                     |
| [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)                     | Use la versión devuelta [**por lineNegotiateAPIVersion.**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)   |
| [**lineGetProviderList**](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist)           | Use la versión más alta compatible con la aplicación.                                     |
| [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)         | Use la versión más alta compatible con la aplicación.                                     |
| [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)   | Use la versión más alta compatible con la aplicación.                                     |
| [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion)   | Use la versión devuelta [**por lineNegotiateAPIVersion.**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)   |
| [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)                                 | Use la versión devuelta [**por lineNegotiateAPIVersion.**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)   |
| [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)         | Use la versión más alta compatible con la aplicación.                                     |
| [**lineTranslateDialog**](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog)           | Use la versión más alta compatible con la aplicación.                                     |
| [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)                   | Use la versión devuelta [**por phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion). |
| [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | Use la versión más alta compatible con la aplicación.                                     |
| [**phoneNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | Use la versión devuelta [**por phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion). |
| [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)                               | Use la versión devuelta [**por phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion). |



 

> [!IMPORTANT]
> Al negociar una versión de API, establezca siempre los números de versión alta y baja en el intervalo de versiones que la aplicación puede admitir. Por ejemplo, nunca use 0x00000000 para la versión baja o 0xFFFFFFFF para el valor alto, ya que estos valores requieren que la aplicación admita todas las versiones de TAPI, tanto pasadas como futuras.

 

 

 



