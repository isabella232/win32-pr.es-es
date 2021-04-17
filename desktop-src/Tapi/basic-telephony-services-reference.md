---
description: Las funciones de telefonía básicas se enumeran por Categoría en las tablas siguientes.
ms.assetid: 09d10789-bc36-47c7-b77d-8698ae75541a
title: Referencia de servicios de telefonía básicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1282a406ea6746f1bb3af11d65164d8af0ce0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687253"
---
# <a name="basic-telephony-services-reference"></a>Referencia de servicios de telefonía básicos

Las funciones de telefonía básicas se enumeran por Categoría en las tablas siguientes. Una función se identifica como [*asincrónica*](a-tapgloss.md) si indica la finalización en un mensaje de respuesta a la aplicación. Si la función devuelve siempre su resultado a la aplicación inmediatamente, la función se considera [*sincrónica*](s-tapgloss.md).

A continuación se encuentra una agrupación funcional de las funciones básicas del servicio de telefonía:

-   [Formatos de dirección](#address-formats)
-   [Direcciones](#addresses)
-   [Responder a las llamadas entrantes](#answering-incoming-calls)
-   [Llamar a funciones Drop](#call-drop-functions)
-   [Manipulación de identificadores de llamadas](#call-handle-manipulation)
-   [Llamar al control de privilegios](#call-privilege-control)
-   [Estados de llamada y eventos](#call-states-and-events)
-   [Estado y capacidades de línea](#line-status-and-capabilities)
-   [Negociación de la versión de línea](#line-version-negotiation)
-   [Información de ubicación y país o región](#location-and-countryregion-information)
-   [Realizar llamadas](#making-calls)
-   [Dispositivos de línea de apertura y cierre](#opening-and-closing-line-devices)
-   [Solicitar servicios de destinatario](#request-recipient-services)
-   [Inicialización y cierre de TAPI](#tapi-initialization-and-shutdown)
-   [Compatibilidad con el protector de peaje](#toll-saver-support)

## <a name="tapi-initialization-and-shutdown"></a>Inicialización y cierre de TAPI



| Función                                     | Descripción                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) | Inicializa la abstracción de línea TAPI para su uso por parte de la aplicación que invoca. Synchronous. |
| [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)         | Cierra el uso de la aplicación de la abstracción de línea de TAPI. Synchronous.               |



 

## <a name="line-version-negotiation"></a>Negociación de la versión de línea



| Función                                                   | Descripción                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------|
| [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) | Permite a una aplicación negociar una versión de TAPI para usarla. Synchronous. |



 

## <a name="line-status-and-capabilities"></a>Estado y capacidades de línea



| Función                                               | Descripción                                                                                                                                                    |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)               | Devuelve las capacidades de un dispositivo de línea determinado. Synchronous.                                                                                                  |
| [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)           | Devuelve la configuración de un dispositivo de flujo de multimedia. Synchronous.                                                                                                   |
| [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)   | Devuelve el estado actual del dispositivo de línea abierto especificado. Synchronous.                                                                                         |
| [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig)           | Establece la configuración del dispositivo de flujo multimedia especificado. Synchronous.                                                                                      |
| [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages) | Especifica los cambios de estado para los que se debe notificar a la aplicación. Synchronous.                                                                      |
| [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) | Devuelve la configuración de mensajes de estado de dirección y línea actual de la aplicación. Synchronous.                                                                       |
| [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)                         | Recupera un identificador de dispositivo asociado a la línea abierta, la dirección o la llamada especificadas. Synchronous.                                                                  |
| [**lineGetIcon**](/windows/desktop/api/Tapi/nf-tapi-linegeticon)                     | Permite que una aplicación recupere un icono para mostrar al usuario. Synchronous.                                                                                |
| [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)           | Hace que el proveedor del dispositivo de línea especificado muestre un cuadro de diálogo que permite al usuario configurar los parámetros relacionados con el dispositivo de línea. Synchronous. |
| [**lineConfigDialogEdit**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialogedit)   | Muestra un cuadro de diálogo que permite al usuario cambiar la información de configuración de un dispositivo de línea. Synchronous.                                                    |



 

## <a name="addresses"></a>Direcciones



| Función                                             | Descripción                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)     | Devuelve las capacidades de telefonía de una dirección. Synchronous.                           |
| [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) | Devuelve el estado actual de una dirección especificada. Synchronous.                              |
| [**lineGetAddressID**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressid)         | Recupera el identificador de dirección de una dirección especificada con un formato alternativo. Synchronous. |



 

## <a name="opening-and-closing-line-devices"></a>Dispositivos de línea de apertura y cierre



| Función                       | Descripción                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------|
| [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)   | Abre un dispositivo de línea especificado para proporcionar una supervisión o control posterior de la línea. Synchronous. |
| [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) | Cierra un dispositivo de línea abierto especificado. Synchronous.                                                        |



 

## <a name="address-formats"></a>Formatos de dirección



| Función                                                 | Descripción                                                                                       |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)     | Traduce entre una dirección en formato canónico y una dirección en formato de marcado. Synchronous. |
| [**lineSetCurrentLocation**](/windows/desktop/api/Tapi/nf-tapi-linesetcurrentlocation) | Establece la ubicación usada como contexto para la traducción de direcciones. Synchronous.                       |
| [**lineSetTollList**](/windows/desktop/api/Tapi/nf-tapi-linesettolllist)               | Manipula la lista de llamadas. Synchronous.                                                           |
| [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)     | Devuelve capacidades de traducción de direcciones. Synchronous.                                            |



 

## <a name="call-states-and-events"></a>Estados de llamada y eventos



| Función                                         | Descripción                                                                         |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)       | Devuelve información fija sobre una llamada. Synchronous.                                |
| [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)   | Devuelve información completa del estado de la llamada de la llamada especificada. Synchronous.       |
| [**lineSetAppSpecific**](/windows/desktop/api/Tapi/nf-tapi-linesetappspecific) | Establece el campo específico de la aplicación de la estructura de información de una llamada. Synchronous. |



 

## <a name="making-calls"></a>Realizar llamadas



| Función                             | Descripción                                                            |
|--------------------------------------|------------------------------------------------------------------------|
| [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) | Realiza una llamada saliente y devuelve un identificador de llamada para ella. Asincrónica |
| [**Fino**](/windows/desktop/api/Tapi/nf-tapi-linedial)         | Dials (partes de una o varias direcciones marcables). Asincrónica         |



 

## <a name="answering-incoming-calls"></a>Responder a las llamadas entrantes



| Función                         | Descripción                             |
|----------------------------------|-----------------------------------------|
| [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) | Responde a una llamada entrante. Asincrónica |



 

## <a name="toll-saver-support"></a>Compatibilidad con el protector de peaje



| Función                                   | Descripción                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings) | Indica el número de anillos después del cual se responderá a las llamadas entrantes. Synchronous.                   |
| [**lineGetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linegetnumrings) | Devuelve el número mínimo de anillos solicitados con [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings). Synchronous. |



 

## <a name="call-privilege-control"></a>Llamar al control de privilegios



| Función                                             | Descripción                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege) | Establece el privilegio de la aplicación en el privilegio especificado. Synchronous. |



 

## <a name="call-drop-functions"></a>Llamar a funciones Drop



| Función                                         | Descripción                                                               |
|--------------------------------------------------|---------------------------------------------------------------------------|
| [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)                     | Desconecta una llamada o abandona un intento de llamada en curso. Asincrónica |
| [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) | Desasigna el identificador de llamada especificado. Synchronous.                       |



 

## <a name="call-handle-manipulation"></a>Manipulación de identificadores de llamadas



| Función                                                   | Descripción                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff)                         | La entrega de la llamada a la propiedad y/o cambia los privilegios de una aplicación a una llamada. Synchronous.                                    |
| [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)                 | Devuelve los identificadores de llamada a las llamadas en una línea o dirección especificada para los que la aplicación todavía no tiene identificadores. Synchronous. |
| [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls) | Devuelve una lista de identificadores de llamada que forman parte de la misma llamada de conferencia que la llamada especificada como un parámetro. Synchronous.    |



 

## <a name="location-and-countryregion-information"></a>Información de ubicación y país o región



| Función                                           | Descripción                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**lineTranslateDialog**](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog) | Muestra un cuadro de diálogo que permite al usuario cambiar la ubicación y la información de la tarjeta de llamada. Synchronous. |
| [**lineGetCountry**](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)           | Recupera las reglas de marcado y otra información acerca de un país o región determinados. Synchronous.              |



 

## <a name="request-recipient-services"></a>Solicitar servicios de destinatario

Las dos funciones siguientes solo se usan para admitir la telefonía asistida.



| Función                                                             | Descripción                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient) | Registra o anula el registro de la aplicación como un destinatario de la solicitud para el modo de solicitud especificado. Synchronous. |
| [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)                             | Obtiene la solicitud siguiente de la biblioteca de vínculos dinámicos de telefonía. Synchronous.                                  |



 

 

 



