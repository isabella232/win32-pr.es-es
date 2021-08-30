---
description: Todos los proveedores de servicios deben implementar funciones básicas de telefonía.
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: Funciones básicas de telefonía de TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f5b8b4b61da6462588115463bc56b7a573e6f81215d0f9a1189983762a21062
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034135"
---
# <a name="tspi-basic-telephony-functions"></a>Funciones básicas de telefonía de TSPI

Todos los proveedores de servicios deben implementar funciones básicas de telefonía. A continuación se muestra una lista de estas funciones por categoría. Una función se identifica como *asincrónica* si indica la finalización en un mensaje REPLY a la aplicación. Si la función siempre devuelve su resultado inmediatamente, la función se considera *sincrónica.*

-   [Direcciones](#addresses)
-   [Respuesta a llamadas entrantes](#answering-incoming-calls)
-   [Llamar a funciones drop](#call-drop-functions)
-   [Llamar a estados y eventos](#call-states-and-events)
-   [Estado y funcionalidades de la línea](#line-status-and-capabilities)
-   [Negociación de versiones de línea](#line-version-negotiation)
-   [Realizar llamadas](#making-calls)
-   [Apertura y cierre de dispositivos de línea](#opening-and-closing-line-devices)
-   [Teléfono Negociación de versiones](#phone-version-negotiation)
-   [Inicialización y apagado de TSP](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a>Inicialización y apagado de TSP



|  Función                                                         |   Descripción                                                        |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [**Proveedor de \_ TUISPIInstalar**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | Instala un TSP. Synchronous.                              |
| [**Proveedor \_ TSPIInstalar**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | Instala el TSP. Obsoleto con la versión 2.0. Synchronous. |
| [**Proveedor \_ TSPIInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | Inicializa el TSP. Synchronous.                         |
| [**Proveedor de \_ TSPIShutdown**](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | Apaga el proveedor de servicios.                          |
| [**Proveedor de \_ TUISPIRemove**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | Quita un TSP. Synchronous.                               |
| [**Proveedor \_ TSPIRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | Quita un TSP. Obsoleto con la versión 2.0. Synchronous.    |



 

## <a name="phone-version-negotiation"></a>Teléfono Negociación de versiones



|  Función                                                         |   Descripción                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**TSPI \_ phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | Devuelve la versión spi más alta en la que el proveedor de servicios puede funcionar para este dispositivo. |



 

## <a name="line-version-negotiation"></a>Negociación de versiones de línea



|  Función                                                         |   Descripción                                                        |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**Línea \_ TSPINegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | Permite que una aplicación negocie una versión de TSPI para usarla con un dispositivo de línea determinado. Synchronous. |



 

## <a name="line-status-and-capabilities"></a>Estado y funcionalidades de la línea



|  Función                                                         |   Descripción                                                        |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Línea \_ TSPIGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | Devuelve las funcionalidades de un dispositivo de línea determinado. Synchronous.                                                                                                  |
| [**Línea \_ TSPIGetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | Devuelve la configuración de un dispositivo de flujo multimedia. Synchronous.                                                                                                   |
| [**Línea \_ TSPIGetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | Devuelve el estado actual del dispositivo de línea abierta especificado. Synchronous.                                                                                         |
| [**TSPI \_ lineSetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | Establece la configuración del dispositivo de secuencia multimedia especificado. Synchronous.                                                                                      |
| [**\_LineSetStatusMessages de TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | Especifica los cambios de estado para los que es necesario notificar a la aplicación. Synchronous.                                                                      |
| [**TSPI \_ lineGetID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | Recupera un identificador de dispositivo asociado a la línea abierta, la dirección o la llamada especificadas. Synchronous.                                                                  |
| [**LineGetIcon de TSPI \_**](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | Permite que una aplicación recupere un icono para mostrarlo al usuario. Synchronous.                                                                                |
| [**LÍNEA DE \_ TUISPIConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | Hace que el proveedor del dispositivo de línea especificado muestre un cuadro de diálogo que permite al usuario configurar parámetros relacionados con el dispositivo de línea. Synchronous. |
| [**LÍNEA DE \_ TUISPIConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | Muestra un cuadro de diálogo que permite al usuario cambiar la información de configuración de un dispositivo de línea. Synchronous.                                                    |



 

## <a name="addresses"></a>Direcciones



|  Función                                                         |   Descripción                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**Línea \_ TSPIGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | Devuelve las funcionalidades de telefonía de una dirección. Synchronous.                           |
| [**Línea \_ TSPIGetAddressStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | Devuelve el estado actual de una dirección especificada. Synchronous.                              |
| [**\_LineGetNumAddressIDs de TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | Recupera el número de identificadores de dirección admitidos en la línea indicada.             |
| [**TSPI \_ lineGetAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | Recupera el identificador de dirección de una dirección especificada mediante un formato alternativo. Synchronous. |



 

## <a name="opening-and-closing-line-devices"></a>Apertura y cierre de dispositivos de línea



|  Función                                                         |   Descripción                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Línea \_ TSPIAbrir**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | Abre un dispositivo de línea especificado para proporcionar la supervisión o el control subsiguientes de la línea. Synchronous. |
| [**TSPI \_ lineClose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | Cierra un dispositivo de línea abierto especificado. Synchronous.                                                        |



 

## <a name="call-states-and-events"></a>Llamar a estados y eventos



|  Función                                                         |   Descripción                                                        |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Línea \_ TSPIGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | Devuelve información fija sobre una llamada. Synchronous.                                |
| [**Línea \_ TSPIGetCallStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | Devuelve información de estado de llamada completa para la llamada especificada. Synchronous.       |
| [**Línea \_ TSPISetAppSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | Establece el campo específico de la aplicación de la estructura de información de una llamada. Synchronous. |



 

## <a name="making-calls"></a>Realizar llamadas



|  Función                                                         |   Descripción                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [**Línea \_ TSPIMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | Realiza una llamada saliente y devuelve un identificador de llamada para ella. Asincrónica |
| [**Línea de \_ TSPIDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | Marcas (partes de una o varias) direcciones que se pueden marcar. Asincrónica         |



 

## <a name="answering-incoming-calls"></a>Respuesta a llamadas entrantes



|  Función                                                         |   Descripción                                                        |
|---------------------------------------------|-----------------------------------------|
| [**Línea de \_ TSPIAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | Responde a una llamada entrante. Asincrónica |



 

## <a name="call-drop-functions"></a>Llamar a funciones drop



|  Función                                                         |   Descripción                                                        |
|-----------------------------------------|---------------------------------------------------------------------------|
| [**Línea \_ TSPIDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | Desconecta una llamada o abandona un intento de llamada en curso. Asincrónica |



 

 

 
