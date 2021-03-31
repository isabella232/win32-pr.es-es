---
description: Todos los proveedores de servicios deben implementar funciones de telefonía básicas.
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: Funciones de telefonía básicas de TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6276be51482620af32650ad1625eea97bddb8e5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913217"
---
# <a name="tspi-basic-telephony-functions"></a>Funciones de telefonía básicas de TSPI

Todos los proveedores de servicios deben implementar funciones de telefonía básicas. A continuación se muestra una lista de estas funciones por categoría. Una función se identifica como *asincrónica* si indica la finalización en un mensaje de respuesta a la aplicación. Si la función devuelve siempre su resultado inmediatamente, la función se considera *sincrónica*.

-   [Direcciones](#addresses)
-   [Responder a las llamadas entrantes](#answering-incoming-calls)
-   [Llamar a funciones Drop](#call-drop-functions)
-   [Estados de llamada y eventos](#call-states-and-events)
-   [Estado y capacidades de línea](#line-status-and-capabilities)
-   [Negociación de la versión de línea](#line-version-negotiation)
-   [Realizar llamadas](#making-calls)
-   [Dispositivos de línea de apertura y cierre](#opening-and-closing-line-devices)
-   [Negociación de la versión de teléfono](#phone-version-negotiation)
-   [Inicialización y cierre de TSP](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a>Inicialización y cierre de TSP



|                                                           |                                                           |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [**TUISPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | Instala un TSP. Synchronous.                              |
| [**TSPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | Instala el TSP. Obsoleto con la versión 2,0. Synchronous. |
| [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | Inicializa el TSP. Synchronous.                         |
| [**TSPI \_ providerShutdown**](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | Cierra el proveedor de servicios.                          |
| [**TUISPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | Quita un TSP. Synchronous.                               |
| [**TSPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | Quita un TSP. Obsoleto con la versión 2,0. Synchronous.    |



 

## <a name="phone-version-negotiation"></a>Negociación de la versión de teléfono



|                                                                           |                                                                                         |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**TSPI \_ phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | Devuelve la versión de SPI más alta en la que el proveedor de servicios puede operar para este dispositivo. |



 

## <a name="line-version-negotiation"></a>Negociación de la versión de línea



|                                                                         |                                                                                                 |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | Permite que una aplicación negocie una versión de TSPI para usarla con un dispositivo de línea determinado. Synchronous. |



 

## <a name="line-status-and-capabilities"></a>Estado y capacidades de línea



|                                                                     |                                                                                                                                                                |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TSPI \_ lineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | Devuelve las capacidades de un dispositivo de línea determinado. Synchronous.                                                                                                  |
| [**TSPI \_ lineGetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | Devuelve la configuración de un dispositivo de flujo de multimedia. Synchronous.                                                                                                   |
| [**TSPI \_ lineGetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | Devuelve el estado actual del dispositivo de línea abierto especificado. Synchronous.                                                                                         |
| [**TSPI \_ lineSetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | Establece la configuración del dispositivo de flujo multimedia especificado. Synchronous.                                                                                      |
| [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | Especifica los cambios de estado para los que se debe notificar a la aplicación. Synchronous.                                                                      |
| [**TSPI \_ lineGetID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | Recupera un identificador de dispositivo asociado a la línea abierta, la dirección o la llamada especificadas. Synchronous.                                                                  |
| [**TSPI \_ lineGetIcon**](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | Permite que una aplicación recupere un icono para mostrar al usuario. Synchronous.                                                                                |
| [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | Hace que el proveedor del dispositivo de línea especificado muestre un cuadro de diálogo que permite al usuario configurar los parámetros relacionados con el dispositivo de línea. Synchronous. |
| [**TUISPI \_ lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | Muestra un cuadro de diálogo que permite al usuario cambiar la información de configuración de un dispositivo de línea. Synchronous.                                                    |



 

## <a name="addresses"></a>Direcciones



|                                                                 |                                                                                          |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | Devuelve las capacidades de telefonía de una dirección. Synchronous.                           |
| [**TSPI \_ lineGetAddressStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | Devuelve el estado actual de una dirección especificada. Synchronous.                              |
| [**TSPI \_ lineGetNumAddressIDs**](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | Recupera el número de identificadores de dirección admitidos en la línea indicada.             |
| [**TSPI \_ lineGetAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | Recupera el identificador de dirección de una dirección especificada con un formato alternativo. Synchronous. |



 

## <a name="opening-and-closing-line-devices"></a>Dispositivos de línea de apertura y cierre



|                                           |                                                                                                            |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**TSPI \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | Abre un dispositivo de línea especificado para proporcionar una supervisión o control posterior de la línea. Synchronous. |
| [**TSPI \_ lineClose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | Cierra un dispositivo de línea abierto especificado. Synchronous.                                                        |



 

## <a name="call-states-and-events"></a>Estados de llamada y eventos



|                                                             |                                                                                     |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**TSPI \_ lineGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | Devuelve información fija sobre una llamada. Synchronous.                                |
| [**TSPI \_ lineGetCallStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | Devuelve información completa del estado de la llamada de la llamada especificada. Synchronous.       |
| [**TSPI \_ lineSetAppSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | Establece el campo específico de la aplicación de la estructura de información de una llamada. Synchronous. |



 

## <a name="making-calls"></a>Realizar llamadas



|                                                 |                                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | Realiza una llamada saliente y devuelve un identificador de llamada para ella. Asincrónica |
| [**TSPI \_ alineado**](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | Dials (partes de una o varias direcciones marcables). Asincrónica         |



 

## <a name="answering-incoming-calls"></a>Responder a las llamadas entrantes



|                                             |                                         |
|---------------------------------------------|-----------------------------------------|
| [**TSPI \_ lineAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | Responde a una llamada entrante. Asincrónica |



 

## <a name="call-drop-functions"></a>Llamar a funciones Drop



|                                         |                                                                           |
|-----------------------------------------|---------------------------------------------------------------------------|
| [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | Desconecta una llamada o abandona un intento de llamada en curso. Asincrónica |



 

 

 
