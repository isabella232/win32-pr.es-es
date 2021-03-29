---
description: Los proveedores de servicios implementan controles detallados del dispositivo de telefonía. Un proveedor de servicios de telefonía (TSP) proporciona controles de llamada y un proveedor de servicios multimedia, si existe, proporciona el control sobre el flujo multimedia.
ms.assetid: eb63d55e-4a2b-4bc0-8001-99772f418d72
title: Proveedores de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424c11d5b99af7440835e8822a5631e1b36f48cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003207"
---
# <a name="service-providers"></a>Proveedores de servicios

Los proveedores de servicios implementan controles detallados del dispositivo de telefonía. Un proveedor de servicios de telefonía (TSP) proporciona controles de llamada y un proveedor de servicios multimedia, si existe, proporciona el control sobre el flujo multimedia.

Todos los proveedores de servicios de telefonía se ejecutan en el proceso TAPISRV. Los proveedores de servicios pueden crear subprocesos en el contexto de TAPISRV según sea necesario para realizar su trabajo y estar seguros de que ninguno de los recursos que crean se destruirá mediante la salida de cualquier aplicación individual. El servidor TAPI traduce los comandos de la aplicación según sea necesario en un conjunto coherente de comandos conocido como la interfaz del proveedor de servicios de telefonía (TSPI).

Los proveedores de servicios multimedia se ejecutan en el espacio de proceso de la aplicación, lo que permite la respuesta rápida a veces necesaria en los controles multimedia. La DLL de TAPI permite el cumplimiento coherente de la interfaz del proveedor de servicios multimedia (MSPI).

Para obtener una cobertura más detallada de los proveedores de servicios, consulte [información general del proveedor de servicios TAPI](./tapi-service-provider-overview.md).

Debajo del archivo DLL del proveedor de servicios de telefonía, el proveedor de servicios puede utilizar cualquier función del sistema u otros componentes necesarios. Estas funciones incluyen [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) y [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol), que funcionan con componentes y servicios de modo kernel diseñados para el proveedor de hardware independiente, así como dispositivos estándar como puertos serie y paralelos para controlar dispositivos externos conectados localmente. También pueden tener acceso a los servicios de red (como RPC, Windows Sockets y canalizaciones con nombre) para la telefonía cliente/servidor.

TAPI carga el archivo DLL de la interfaz de usuario del proveedor de servicios de telefonía en el proceso de una aplicación que invoca cualquiera de las funciones del proveedor de servicios que pueden mostrar un cuadro de diálogo (por ejemplo, [**TSPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog)). El proveedor de servicios también puede hacer que la DLL de la interfaz de usuario asociada se cargue y se ejecute en el proceso de una aplicación si el proveedor de servicios necesita mostrar la interfaz de usuario en momentos inesperados. por ejemplo, para mostrar el cuadro de diálogo **Talk/hange** que muestra el controlador de módem universal (Unimodem) cuando se usa un módem de datos para marcar una llamada de voz interactiva con [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) (que normalmente no se considera una función de generación de la interfaz de usuario).

El controlador de solicitudes de proxy es una aplicación de telefonía completa que se ejecuta normalmente en un servidor de telefonía (el mismo servidor en el que se ejecuta el proveedor de servicios de telefonía para los dispositivos de línea asociados). Esta arquitectura, en lugar de la arquitectura del proveedor de servicios de WOSA, se usa cuando un servicio determinado se implementa de forma más adecuada en una aplicación que en un controlador del servidor. Por ejemplo, las funciones de administración de agentes ACD se implementan en un controlador de solicitudes de proxy en lugar de en un proveedor de servicios.

El proveedor de servicios de controlador Unimodem para el control de módem está disponible en los sistemas operativos Windows Server 2003, Windows XP, Windows 2000 y Windows NT. La telefonía de Windows también incluye un asignador de interfaz del proveedor de servicios de telefonía (TSPI) de modo kernel genérico, KMDDSP, que permite implementar proveedores de servicios como controladores de dispositivos de modo kernel.

 

 
