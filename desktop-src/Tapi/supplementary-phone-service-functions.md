---
description: Las funciones adicionales del servicio telefónico se enumeran por categoría en los temas siguientes.
ms.assetid: 0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5
title: Funciones de Teléfono adicionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ee0e32260ac3821fd06e7e8962ab2a6186fb42f1140eb6cd8f705709f2dfbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861423"
---
# <a name="supplementary-phone-service-functions"></a>Funciones de Teléfono adicionales

Las funciones adicionales del servicio telefónico se enumeran por categoría en los temas siguientes. Una función se identifica como [*asincrónica*](a-tapgloss.md) si indica la finalización en un mensaje REPLY a la aplicación. Si la función siempre devuelve su resultado a la aplicación inmediatamente, la función se considera [*sincrónica.*](s-tapgloss.md)

A continuación se muestra una agrupación funcional de las funciones adicionales del servicio telefónico:

-   [Botones](#buttons)
-   [Áreas de datos](#data-areas)
-   [Pantalla](#display)
-   [Dispositivos hookswitch](#hookswitch-devices)
-   [Lámparas](#lamps)
-   [Apertura y cierre de dispositivos telefónicos](#opening-and-closing-phone-devices)
-   [Teléfono inicialización y apagado](#phone-initialization-and-shutdown)
-   [Teléfono y funcionalidades](#phone-status-and-capabilities)
-   [Teléfono negociación de versiones](#phone-version-negotiation)
-   [En anillo](#ring)
-   [Estado](#status)

## <a name="phone-initialization-and-shutdown"></a>Teléfono Inicialización y apagado



| Función                                       | Descripción                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------|
| [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) | Inicializa la abstracción del teléfono TAPI para que la aplicación de invocación la use. Synchronous. |
| [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)         | Apaga el uso de la abstracción telefónica de TAPI por parte de una aplicación. Synchronous.            |



 

## <a name="phone-version-negotiation"></a>Teléfono Negociación de versiones



| Función                                                     | Descripción                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | Permite que una aplicación negocie una versión de TAPI para usarla. Synchronous. |



 

## <a name="opening-and-closing-phone-devices"></a>Apertura y cierre de Teléfono dispositivos



| Función                         | Descripción                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)   | Abre el dispositivo telefónico especificado, lo que da a la aplicación privilegios de propietario o de supervisión. Synchronous. |
| [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) | Cierra un dispositivo de teléfono abierto especificado. Synchronous.                                                        |



 

## <a name="phone-status-and-capabilities"></a>Teléfono Estado y funcionalidades



| Función                                       | Descripción                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)     | Devuelve las funcionalidades de un dispositivo de teléfono determinado. Synchronous.                                                                                                   |
| [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)               | Devuelve un identificador de dispositivo para la clase de dispositivo determinada asociada al dispositivo de teléfono especificado. Synchronous.                                                          |
| [**phoneGetIcon**](/windows/desktop/api/Tapi/nf-tapi-phonegeticon)           | Permite que una aplicación recupere un icono para mostrarlo al usuario. Synchronous.                                                                                  |
| [**phoneConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) | Hace que el proveedor del dispositivo telefónico especificado muestre un cuadro de diálogo que permite al usuario configurar parámetros relacionados con el dispositivo telefónico. Synchronous. |



 

## <a name="hookswitch-devices"></a>Dispositivos hookswitch



| Función                                         | Descripción                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) | Establece el estado de enlace de los dispositivos de conmutador de enlace de un teléfono abierto en un modo especificado. Asincrónica      |
| [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) | Consulta el modo hookswitch de un dispositivo hookswitch de un dispositivo de teléfono abierto. Synchronous.          |
| [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume)         | Establece el volumen del altavoz de un dispositivo de conmutador de enlace de un dispositivo de teléfono abierto. Asincrónica           |
| [**phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume)         | Devuelve la configuración del volumen del altavoz de un dispositivo de enlace de un dispositivo de teléfono abierto. Synchronous. |
| [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain)             | Establece la ganancia del micrófono de un dispositivo de conmutador de enlace de un dispositivo de teléfono abierto. Asincrónica                 |
| [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain)             | Devuelve la configuración de ganancia del micrófono de un dispositivo de conmutador de enlace de un teléfono abierto. Synchronous.              |



 

## <a name="display"></a>Mostrar



| Función                                   | Descripción                                                              |
|--------------------------------------------|--------------------------------------------------------------------------|
| [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) | Escribe información en la pantalla de un dispositivo de teléfono abierto. Asincrónica |
| [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) | Devuelve el contenido actual de la pantalla de un teléfono. Synchronous.          |



 

## <a name="ring"></a>En anillo



| Función                             | Descripción                                                              |
|--------------------------------------|--------------------------------------------------------------------------|
| [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring) | Anillos de un dispositivo de teléfono abierto según un modo de anillo determinado. Asincrónica |
| [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring) | Devuelve el modo de anillo actual de un dispositivo telefónico abierto. Synchronous.    |



 

## <a name="buttons"></a>Botones



| Función                                         | Descripción                                                                    |
|--------------------------------------------------|--------------------------------------------------------------------------------|
| [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo) | Establece la información asociada a un botón en un dispositivo de teléfono. Asincrónica |
| [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo) | Devuelve información asociada a un botón en un dispositivo de teléfono. Synchronous.   |



 

## <a name="lamps"></a>Lámparas



| Función                             | Descripción                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------|
| [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp) | Enciende una bombilla en un dispositivo de teléfono abierto especificado en un modo de iluminación de bombilla determinado. Asincrónica |
| [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp) | Devuelve el modo de bombilla actual de la bombilla especificada. Synchronous.                           |



 

## <a name="data-areas"></a>Áreas de datos



| Función                             | Descripción                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------|
| [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) | Descarga un búfer de datos en un área de datos determinada del dispositivo telefónico. Asincrónica      |
| [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) | Carga el contenido de un área de datos determinada en el dispositivo de teléfono en un búfer. Synchronous. |



 

## <a name="status"></a>Estado



| Función                                                 | Descripción                                                                               |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) | Especifica los cambios de estado para los que se quiere notificar a la aplicación. Synchronous. |
| [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) | Devuelve los cambios de estado para los que se quiere notificar a la aplicación. Synchronous.   |
| [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)                 | Devuelve el estado completo de un dispositivo de teléfono abierto. Synchronous.                         |



 

 

 



