---
description: Las funciones de servicio de teléfono complementarias se enumeran por Categoría en los temas siguientes.
ms.assetid: 0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5
title: Funciones de servicio de teléfono complementarias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527c39441a924a4f9787d22bf8db596882e7f257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677795"
---
# <a name="supplementary-phone-service-functions"></a>Funciones de servicio de teléfono complementarias

Las funciones de servicio de teléfono complementarias se enumeran por Categoría en los temas siguientes. Una función se identifica como [*asincrónica*](a-tapgloss.md) si indica la finalización en un mensaje de respuesta a la aplicación. Si la función devuelve siempre su resultado a la aplicación inmediatamente, la función se considera [*sincrónica*](s-tapgloss.md).

A continuación se encuentra una agrupación funcional de las funciones de servicio de teléfono complementarias:

-   [Botones](#buttons)
-   [Áreas de datos](#data-areas)
-   [Pantalla](#display)
-   [Dispositivos conmutador](#hookswitch-devices)
-   [Lámparas](#lamps)
-   [Apertura y cierre de dispositivos telefónicos](#opening-and-closing-phone-devices)
-   [Inicialización y cierre del teléfono](#phone-initialization-and-shutdown)
-   [Estado y capacidades del teléfono](#phone-status-and-capabilities)
-   [Negociación de la versión de teléfono](#phone-version-negotiation)
-   [Pistón](#ring)
-   [Estado](#status)

## <a name="phone-initialization-and-shutdown"></a>Inicialización y cierre del teléfono



| Función                                       | Descripción                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------|
| [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) | Inicializa la abstracción del teléfono TAPI para su uso por parte de la aplicación que invoca. Synchronous. |
| [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)         | Cierra el uso de una aplicación de la abstracción de teléfono de TAPI. Synchronous.            |



 

## <a name="phone-version-negotiation"></a>Negociación de la versión de teléfono



| Función                                                     | Descripción                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | Permite a una aplicación negociar una versión de TAPI para usarla. Synchronous. |



 

## <a name="opening-and-closing-phone-devices"></a>Apertura y cierre de dispositivos telefónicos



| Función                         | Descripción                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)   | Abre el dispositivo de teléfono especificado, lo que permite a la aplicación tener privilegios de propietario o de supervisión. Synchronous. |
| [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) | Cierra un dispositivo telefónico abierto especificado. Synchronous.                                                        |



 

## <a name="phone-status-and-capabilities"></a>Estado y capacidades del teléfono



| Función                                       | Descripción                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)     | Devuelve las capacidades de un dispositivo telefónico determinado. Synchronous.                                                                                                   |
| [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)               | Devuelve un identificador de dispositivo para la clase de dispositivo especificada asociada al dispositivo telefónico especificado. Synchronous.                                                          |
| [**phoneGetIcon**](/windows/desktop/api/Tapi/nf-tapi-phonegeticon)           | Permite que una aplicación recupere un icono para mostrar al usuario. Synchronous.                                                                                  |
| [**phoneConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) | Hace que el proveedor del dispositivo telefónico especificado muestre un cuadro de diálogo que permite al usuario configurar los parámetros relacionados con el dispositivo telefónico. Synchronous. |



 

## <a name="hookswitch-devices"></a>Dispositivos conmutador



| Función                                         | Descripción                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) | Establece el estado de enlace de los dispositivos conmutador de un teléfono abierto en un modo especificado. Asincrónica      |
| [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) | Consulta el modo conmutador de un dispositivo conmutador de un dispositivo teléfono abierto. Synchronous.          |
| [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume)         | Establece el volumen del altavoz de un dispositivo conmutador de un dispositivo teléfono abierto. Asincrónica           |
| [**phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume)         | Devuelve la configuración del volumen del altavoz de un dispositivo conmutador de un dispositivo teléfono abierto. Synchronous. |
| [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain)             | Establece la ganancia del MIC de un dispositivo conmutador de un dispositivo telefónico abierto. Asincrónica                 |
| [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain)             | Devuelve el valor de ganancia del MIC de un dispositivo conmutador de un teléfono abierto. Synchronous.              |



 

## <a name="display"></a>Pantalla



| Función                                   | Descripción                                                              |
|--------------------------------------------|--------------------------------------------------------------------------|
| [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) | Escribe información en la pantalla de un dispositivo telefónico abierto. Asincrónica |
| [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) | Devuelve el contenido actual de la pantalla de un teléfono. Synchronous.          |



 

## <a name="ring"></a>En anillo



| Función                             | Descripción                                                              |
|--------------------------------------|--------------------------------------------------------------------------|
| [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring) | Suena un dispositivo teléfono abierto según un modo de anillo determinado. Asincrónica |
| [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring) | Devuelve el modo de anillo actual de un dispositivo telefónico abierto. Synchronous.    |



 

## <a name="buttons"></a>Botones



| Función                                         | Descripción                                                                    |
|--------------------------------------------------|--------------------------------------------------------------------------------|
| [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo) | Establece la información asociada a un botón en un dispositivo telefónico. Asincrónica |
| [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo) | Devuelve información asociada a un botón en un dispositivo telefónico. Synchronous.   |



 

## <a name="lamps"></a>Lámparas



| Función                             | Descripción                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------|
| [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp) | Enciende una lámpara en un dispositivo telefónico abierto específico en un modo de iluminación de lámpara determinado. Asincrónica |
| [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp) | Devuelve el modo de lámpara actual de la lámpara especificada. Synchronous.                           |



 

## <a name="data-areas"></a>Áreas de datos



| Función                             | Descripción                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------|
| [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) | Descarga un búfer de datos en un área de datos determinada del dispositivo telefónico. Asincrónica      |
| [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) | Carga el contenido de un área de datos determinada en el dispositivo telefónico en un búfer. Synchronous. |



 

## <a name="status"></a>Status



| Función                                                 | Descripción                                                                               |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) | Especifica los cambios de estado para los que la aplicación desea recibir notificaciones. Synchronous. |
| [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) | Devuelve los cambios de estado para los que la aplicación desea recibir notificaciones. Synchronous.   |
| [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)                 | Devuelve el estado completo de un dispositivo telefónico abierto. Synchronous.                         |



 

 

 



