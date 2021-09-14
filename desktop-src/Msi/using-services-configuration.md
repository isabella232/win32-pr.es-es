---
description: La configuración de servicios permite que Windows Installer personalice los servicios en un equipo.
ms.assetid: 164280b2-1c75-49d2-ac04-c3654be84134
title: Uso de la configuración de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f6e3040d51b1056a370490fc5328a6bafe07555
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254013"
---
# <a name="using-services-configuration"></a>Uso de la configuración de servicios

La configuración de servicios permite Windows Installer para personalizar los [servicios](../services/services.md) en un equipo. Los desarrolladores pueden crear un paquete del instalador de Windows para instalar, detener, iniciar y eliminar servicios durante una instalación mediante las tablas [ServiceControl](servicecontrol-table.md) y [ServiceInstall](serviceinstall-table.md) y las acciones [InstallServices,](installservices-action.md) [StopServices](stopservices-action.md) y [DeleteServices.](deleteservices-action.md)

A partir de los paquetes escritos para Windows Installer 5.0, los desarrolladores también pueden usar la acción estándar [MsiConfigureServices](msiconfigureservices-action.md) y la tabla [MsiServiceConfig](msiserviceconfig-table.md) para configurar las opciones de personalización de servicio extendidas disponibles con Windows 7 y Windows Server 2008 R2 y Windows Vista y Windows Server 2008. Los paquetes de instalación existentes escritos para versiones del instalador de Windows que no incluyeban la tabla MsiServiceConfig todavía se pueden instalar mediante Windows Installer 5.0. La característica de configuración de servicios del instalador de Windows no puede configurar cuentas de servicio de red, instalar procesos de host de servicio compartido (svchost) o reiniciar servicios detenidos como parte de la instalación.

**Windows XP y Windows Server 2003 o versiones anteriores:** No se admite. Las tablas de configuración de servicio y las acciones estándar están disponibles a partir de Windows Installer 5.0 que se ejecuta en Windows 7 y Windows Server 2008 R2 y Windows Installer 4.5 que se ejecuta en Windows Vista y Windows Server 2008.

Debe incluir la acción [MsiConfigureServices](msiconfigureservices-action.md) en la tabla [InstallExecuteSequence](installexecutesequence-table.md) para solicitar las configuraciones de servicio que especifique en la [tabla MsiServiceConfig](msiserviceconfig-table.md). El Windows utiliza la información de la tabla MsiServiceConfig solo cuando la acción estándar MsiConfigureServices se incluye en una tabla de secuencia. La acción estándar MsiConfigureServices también usa información en las tablas [ServiceControl](servicecontrol-table.md) [y ServiceInstall.](serviceinstall-table.md)

Para solicitar que el sistema solo dé los privilegios necesarios a un servicio determinado, especifique el servicio y la opción de configuración **SERVICE \_ CONFIG REQUIRED \_ \_ PRIVILEGES \_ INFO** en la [tabla MsiServiceConfig](msiserviceconfig-table.md). Quite los privilegios innecesarios del token de proceso del servicio. Esta opción se puede usar para configurar los servicios que se ejecutan en el contexto de seguridad de las cuentas de usuario del servicio LocalSystem, LocalService [o NetworkService](../services/service-user-accounts.md).

Para solicitar que el sistema retrase el inicio automático de un servicio durante un tiempo después del inicio de todos los demás servicios de inicio automático, especifique el servicio y la opción **SERVICE \_ CONFIG \_ DELAYED AUTO \_ \_ START** en la tabla [MsiServiceConfig](msiserviceconfig-table.md). El paquete actual debe instalar el servicio que se está retrasando con SERVICE AUTO START especificado en la tabla ServiceInstall o el servicio ya debe estar instalado como servicio \_ \_ de inicio automático. [](serviceinstall-table.md)

Para solicitar que el sistema reserve un recurso para el uso exclusivo de un servicio determinado, especifique el servicio, el tipo de SID de servicio y la opción de configuración **SERVICE \_ CONFIG SERVICE \_ \_ SID \_ INFO** en la tabla [MsiServiceConfig](msiserviceconfig-table.md). Agregue el SID del servicio a la lista de Access Control recursos (ACL) del recurso.

Para solicitar que [Service Control Manager](../services/service-control-manager.md) (SCM) espere después de enviar la notificación DE **\_ \_ PRESHUTDOWN DE SERVICE CONTROL** a un servicio, haga lo siguiente. Especifique el servicio, el tiempo que debe esperar el SCM y la opción de configuración **\_ SERVICE CONFIG \_ PRESHUTDOWN \_ INFO** en la [tabla MsiServiceConfig](msiserviceconfig-table.md).

Para configurar cuándo el sistema debe ejecutar acciones después del error de un servicio, especifique el servicio y la opción **SERVICE CONFIG FAILURE ACTIONS \_ \_ \_ \_ FLAG** en la [tabla MsiServiceConfig](msiserviceconfig-table.md). Agregue las acciones que se ejecutarán a la [tabla MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md).

Para obtener más información sobre las funcionalidades de personalización de servicios extendidas introducidas con los sistemas operativos Windows Vista y Windows Server 2008, vea Cambios de servicio [para Windows Vista](../services/service-changes-for-windows-vista.md).

 

 
