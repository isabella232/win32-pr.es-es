---
description: Los proveedores de servicios implementan controles detallados de dispositivos de telefonía. Un proveedor de servicios de telefonía (TSP) proporciona controles de llamada y un proveedor de servicios multimedia, si existe, proporciona control sobre la secuencia multimedia.
ms.assetid: eb63d55e-4a2b-4bc0-8001-99772f418d72
title: Proveedores de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0bc427b79daadc8dc89e49a29e18ebbd9797bed74da7f890dc851d6ee97b13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773125"
---
# <a name="service-providers"></a>Proveedores de servicios

Los proveedores de servicios implementan controles detallados de dispositivos de telefonía. Un proveedor de servicios de telefonía (TSP) proporciona controles de llamada y un proveedor de servicios multimedia, si existe, proporciona control sobre la secuencia multimedia.

Todos los proveedores de servicios de telefonía se ejecutan en el proceso TAPISRV. Los proveedores de servicios pueden crear subprocesos en el contexto TAPISRV según sea necesario para realizar su trabajo y estar seguros de que ninguno de los recursos que cree se destruirá con la salida de cualquier aplicación individual. El servidor TAPI traduce los comandos de aplicación según sea necesario en un conjunto coherente de comandos conocidos como interfaz del proveedor de servicios de telefonía (TSPI).

Los proveedores de servicios multimedia se ejecutan en el espacio de proceso de la aplicación, lo que permite la respuesta rápida que a veces se requiere en los controles multimedia. El archivo DLL de TAPI proporciona una adhesión coherente a la interfaz del proveedor de servicios multimedia (MSPI).

Para obtener una cobertura más detallada de los proveedores de servicios, consulte [Información general del proveedor de servicios TAPI.](./tapi-service-provider-overview.md)

Debajo de la DLL del proveedor de servicios de telefonía, el proveedor de servicios puede usar las funciones del sistema u otros componentes necesarios. Estas funciones incluyen [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) y [**DeviceIoControl,**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)que funcionan con servicios y componentes de modo kernel diseñados por el proveedor de hardware independientes, así como dispositivos estándar, como puertos serie y paralelos, para controlar dispositivos externos conectados localmente. También pueden acceder a servicios de red (como RPC, Windows Sockets y canalizaciones con nombre) para la telefonía cliente/servidor.

TAPI carga el archivo DLL de interfaz de usuario del proveedor de servicios de telefonía en el proceso de una aplicación que invoca cualquiera de las funciones del proveedor de servicios que pueden mostrar un cuadro de diálogo (por ejemplo, [**TSPI \_ lineConfigDialog).**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog) El proveedor de servicios también puede hacer que su DLL de interfaz de usuario asociada se cargue y ejecute en el proceso de una aplicación si el proveedor de servicios necesita mostrar la interfaz de usuario en momentos inesperados, como para mostrar el cuadro de diálogo **Talk/Hang-up** que muestra el controlador de módem universal (UNIMODEM) cuando se usa un módem de datos para marcar una llamada de voz interactiva mediante la línea [**\_ TSPIMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) (no se considera normalmente una función que genera la interfaz de usuario).

El controlador de solicitudes de proxy es una aplicación de telefonía completa que normalmente se ejecuta en un servidor de telefonía (el mismo servidor en el que se ejecuta el proveedor de servicios de telefonía para los dispositivos de línea asociados). Esta arquitectura, en lugar de la arquitectura del proveedor de servicios WOSA, se usa cuando un servicio determinado se implementa más adecuadamente en una aplicación que en un controlador en el servidor. Por ejemplo, las funciones de administración del agente de ACD se implementan en un controlador de solicitudes de proxy en lugar de en un proveedor de servicios.

El proveedor de servicios de controlador UNIMODEM para el control de módem está disponible en los sistemas operativos Windows Server 2003, Windows XP, Windows 2000 y Windows NT. Windows La telefonía también incluye un asignador de interfaz de proveedor de servicios de telefonía (TSPI) en modo kernel genérico, KMDDSP, que permite que los proveedores de servicios se implementen como controladores de dispositivo en modo kernel.

 

 
