---
description: Como parte de la abstracción de dispositivos telefónicos definida por TSPI, TAPI y el proveedor de servicios deben someterse primero a la inicialización básica.
ms.assetid: cd8bb328-fbd0-409c-8471-34ad4c2c8d93
title: Inicialización de SPI de teléfono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d0c54e313c2be3846aeb604217f5324ec0d8a8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688000"
---
# <a name="phone-spi-initialization"></a>Inicialización de SPI de teléfono

Como parte de la abstracción de dispositivos telefónicos definida por TSPI, TAPI y el proveedor de servicios deben someterse primero a la inicialización básica. Esta inicialización básica se realiza tanto para la mitad de la línea como para la mitad de la interfaz mediante el mismo conjunto de pasos. El primero de estos pasos es la negociación de la versión de la interfaz. Para ello, TAPI llama a la función [**\_ LineNegotiateTSPIVersion de TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) . Esta función se utiliza normalmente para negociar en nombre de un dispositivo de línea individual; distintos dispositivos de línea dentro del mismo proveedor de servicios pueden funcionar según las distintas versiones de la interfaz. TAPI pasa un valor de identificador de dispositivo reservado especial, [**inicializar \_ negociación**](initialize-negotiation.md), para indicar que está negociando una versión de interfaz global para las funciones de inicialización que afectan a todo el proveedor de servicios, tanto para las líneas como para los teléfonos.

El resultado de esta negociación se pasa a los procedimientos posteriores hasta que se abre un dispositivo telefónico. En ese momento, el dispositivo telefónico se confirmará en una versión de interfaz determinada. Esta versión de la interfaz es implícita hasta que se cierra el teléfono y no es necesario pasarla a las funciones subsiguientes que operan en un teléfono abierto.

Después de la negociación de la versión general de la interfaz, TAPI llama a la función [**\_ ProviderInit de TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit) . Esta función inicializa el proveedor de servicios, lo que también le permite los parámetros necesarios para la operación subsiguiente. Estos parámetros incluyen los siguientes:

-   *dwPermanentProviderID*: especifica el identificador permanente del proveedor de servicios que se está inicializando, único dentro de los proveedores de servicios de este sistema.
-   *dwLineDeviceIDBase*: especifica el identificador de dispositivo más bajo para los dispositivos de línea admitidos por este proveedor de servicios.
-   *dwPhoneDeviceIDBase*: especifica el identificador de dispositivo más bajo para los dispositivos telefónicos admitidos por este proveedor de servicios. Los dispositivos de la clase de dispositivo teléfono de telefonía se identifican mediante enteros a partir de cero. Este intervalo de identificadores es contiguo en todo el intervalo de dispositivos de teléfono. Dado que puede haber varios proveedores de servicios que administran dispositivos telefónicos en un único sistema, cada proveedor de servicios obtiene una parte contigua del intervalo total. Este parámetro indica al proveedor de servicios el valor más bajo de su parte del intervalo. El proveedor de servicios, en lugar de TAPI, es responsable de asignar este intervalo de variables a sus propios identificadores de dispositivo internos. Esto proporciona al proveedor del proveedor de servicios la flexibilidad suficiente para usar identificadores de dispositivo en extensiones específicas del dispositivo, si así lo desea. Dado que el proveedor de servicios sabe qué identificadores de dispositivo aparecen en las estructuras de datos y los parámetros definidos por TAPI, puede usar identificadores de dispositivo coherentes en las estructuras de datos y los parámetros de extensión específicos del dispositivo.
-   *dwNumLines*: especifica el número de dispositivos de línea que admite este proveedor de servicios.
-   *dwNumPhones*: especifica cuántos dispositivos telefónicos admite este proveedor de servicios.
-   *lpfnCompletionProc*: especifica el procedimiento al que el proveedor de servicios llama para informar de la finalización de todos los procedimientos operativos de forma asincrónica en los dispositivos de línea y teléfono.

Después de [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), se pueden realizar operaciones normales, como la apertura de teléfonos.

 

 
