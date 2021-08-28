---
description: Como parte de la abstracción de dispositivos telefónicos definida por TSPI, TAPI y el proveedor de servicios deben someterse primero a la inicialización básica.
ms.assetid: cd8bb328-fbd0-409c-8471-34ad4c2c8d93
title: Teléfono Inicialización de SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88465e31857ee9ecc3a54f98f98bf6d1d3b50b837d845dbf36af08be0ec78a7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072895"
---
# <a name="phone-spi-initialization"></a>Teléfono Inicialización de SPI

Como parte de la abstracción de dispositivos telefónicos definida por TSPI, TAPI y el proveedor de servicios deben someterse primero a la inicialización básica. Esta inicialización básica se realiza para las mitades de línea y teléfono de la interfaz mediante el mismo conjunto de pasos. El primero de estos pasos es la negociación de versiones de interfaz. TAPI realiza esta operación llamando a la función [**\_ lineNegotiateTSPIVersion de TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) Esta función se usa normalmente para negociar en nombre de un dispositivo de línea individual; diferentes dispositivos de línea dentro del mismo proveedor de servicios pueden funcionar según diferentes versiones de interfaz. TAPI pasa un valor de identificador de dispositivo reservado especial, [**INITIALIZE \_ NEGOTIATION**](initialize-negotiation.md), para indicar que está negociando una versión de interfaz general para las funciones de inicialización que afectan a todo el proveedor de servicios, tanto para líneas como para teléfonos.

El resultado de esta negociación se pasa a procedimientos posteriores hasta que se abre un dispositivo telefónico. En ese momento, el dispositivo telefónico se confirma en una versión de interfaz determinada. Esta versión de interfaz es implícita hasta que se cierra el teléfono y no es necesario pasarla a funciones posteriores que funcionan en un teléfono abierto.

Después de la negociación general de la versión de la interfaz, TAPI llama a la [**función \_ providerInit de TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit) Esta función inicializa el proveedor de servicios y también le proporciona los parámetros necesarios para la operación posterior. Estos parámetros incluyen los siguientes:

-   *dwPermanentProviderID:* especifica el identificador permanente del proveedor de servicios que se inicializa, único dentro de los proveedores de servicios de este sistema.
-   *dwLineDeviceIDBase:* especifica el identificador de dispositivo más bajo para los dispositivos de línea compatibles con este proveedor de servicios.
-   *dwPhoneDeviceIDBase:* especifica el identificador de dispositivo más bajo para los dispositivos de teléfono compatibles con este proveedor de servicios. Los dispositivos de la clase de dispositivo de teléfono de telefonía se identifican mediante enteros a partir de cero. Este intervalo de identificadores es contiguo en toda la gama de dispositivos de teléfono. Dado que puede haber varios proveedores de servicios que administran dispositivos telefónicos en un único sistema, cada proveedor de servicios obtiene una parte contigua del intervalo total. Este parámetro indica al proveedor de servicios el valor más bajo en su parte del intervalo. El proveedor de servicios, en lugar de TAPI, es responsable de asignar este intervalo de variables a sus propios identificadores de dispositivo internos. Esto proporciona al proveedor de servicios flexibilidad suficiente para usar identificadores de dispositivo en extensiones específicas del dispositivo si lo desea. Dado que el proveedor de servicios sabe qué identificadores de dispositivo aparecen en las estructuras de datos y los parámetros definidos por TAPI, puede usar identificadores de dispositivo coherentes en estructuras de datos y parámetros de extensión específicos del dispositivo.
-   *dwNumLines:* especifica cuántos dispositivos de línea admite este proveedor de servicios.
-   *dwNumPhones:* especifica cuántos dispositivos telefónicos admite este proveedor de servicios.
-   *lpfnCompletionProc:* especifica el procedimiento al que llama el proveedor de servicios para notificar la finalización de todos los procedimientos operativos asincrónicos en dispositivos de línea y teléfono.

Siguiendo [**el proveedor de TSPIInit, \_**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)se pueden realizar operaciones normales, como abrir teléfonos.

 

 
