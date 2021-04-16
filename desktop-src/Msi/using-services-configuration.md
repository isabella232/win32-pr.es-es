---
description: La configuración de servicios permite al Windows Installer personalizar los servicios de un equipo.
ms.assetid: 164280b2-1c75-49d2-ac04-c3654be84134
title: Uso de la configuración de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f6e3040d51b1056a370490fc5328a6bafe07555
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496894"
---
# <a name="using-services-configuration"></a>Uso de la configuración de servicios

La configuración de servicios permite al Windows Installer personalizar los [servicios](../services/services.md) de un equipo. Los desarrolladores pueden crear un paquete de Windows Installer para instalar, detener, iniciar y eliminar servicios durante una instalación mediante las tablas [ServiceControl](servicecontrol-table.md) y [ServiceInstall](serviceinstall-table.md) y las acciones [InstallServices](installservices-action.md), [StopServices](stopservices-action.md) y [DeleteServices](deleteservices-action.md) .

A partir de los paquetes escritos para Windows Installer 5,0, los desarrolladores también pueden usar la acción estándar [MsiConfigureServices](msiconfigureservices-action.md) y la [tabla MsiServiceConfig](msiserviceconfig-table.md) para configurar las opciones de personalización de servicio extendidas disponibles con Windows 7 y Windows Server 2008 R2 y Windows Vista y Windows Server 2008. Los paquetes de instalación existentes escritos para las versiones del Windows Installer que no incluían la tabla MsiServiceConfig se pueden instalar con Windows Installer 5,0. La característica de configuración de servicios del Windows Installer no puede configurar cuentas de servicio de red, instalar procesos de host de servicios compartidos (svchost) o reiniciar servicios detenidos como parte de la instalación.

**Windows XP y Windows Server 2003 o anterior:** No compatible. Las tablas de configuración del servicio y las acciones estándar están disponibles a partir de Windows Installer 5,0 que se ejecuta en Windows 7 y Windows Server 2008 R2 y Windows Installer 4,5 que se ejecutan en Windows Vista y Windows Server 2008.

Debe incluir la acción [MsiConfigureServices](msiconfigureservices-action.md) en la tabla [InstallExecuteSequence](installexecutesequence-table.md) para solicitar las configuraciones de servicio que especifique en la [tabla MsiServiceConfig](msiserviceconfig-table.md). El Windows Installer usa la información de la tabla MsiServiceConfig solo cuando la acción de MsiConfigureServices estándar está incluida en una tabla de secuencia. La acción estándar MsiConfigureServices también usa información en las tablas [ServiceControl](servicecontrol-table.md) y [ServiceInstall](serviceinstall-table.md) .

Para solicitar que el sistema proporcione solo los privilegios necesarios para un servicio determinado, especifique el servicio y la opción de configuración del servicio configuración de **\_ \_ \_ \_ privilegios necesaria** en la [tabla MsiServiceConfig](msiserviceconfig-table.md). Quite los privilegios innecesarios del token de proceso del servicio. Esta opción se puede usar para configurar los servicios que se ejecutan en el contexto de seguridad de las [cuentas de usuario del servicio](../services/service-user-accounts.md)LocalSystem, LocalService o NetworkService.

Para solicitar que el sistema retrase el inicio automático de un servicio durante un tiempo después del inicio de todos los demás servicios de inicio automático, especifique el servicio y la opción de **\_ \_ \_ \_ Inicio automático retrasado** de la configuración del servicio en la [tabla MsiServiceConfig](msiserviceconfig-table.md). El servicio que se retrasa debe instalarse mediante el paquete actual con el servicio de \_ \_ Inicio automático especificado en la tabla [ServiceInstall](serviceinstall-table.md) o el servicio ya debe estar instalado como un servicio de inicio automático.

Para solicitar que el sistema Reserve un recurso para el uso exclusivo de un servicio determinado, especifique el servicio, el tipo de SID de servicio y la opción de configuración **\_ información de \_ \_ SID \_ del servicio** de configuración de servicio en la [tabla MsiServiceConfig](msiserviceconfig-table.md). Agregue el SID del servicio a la lista de Access Control (ACL) del recurso.

Para solicitar que el [Administrador de control de servicios](../services/service-control-manager.md) (SCM) espere después de enviar la notificación de **cierre del \_ control \_ del servicio** a un servicio, haga lo siguiente. Especifique el servicio, la cantidad de tiempo que debe esperar el SCM y la opción de configuración **\_ \_ \_ información de preapagado de configuración del servicio** en la [tabla MsiServiceConfig](msiserviceconfig-table.md).

Para configurar el momento en que el sistema debe ejecutar acciones después del error de un servicio, especifique el servicio y la opción de marca de acciones de error de configuración del servicio en la [tabla MsiServiceConfig](msiserviceconfig-table.md). **\_ \_ \_ \_** Agregue las acciones que se van a ejecutar en la [tabla MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md).

Para obtener más información acerca de las capacidades de personalización de servicio extendidas que se introdujeron con los sistemas operativos Windows Vista y Windows Server 2008, consulte [cambios de servicio para Windows Vista](../services/service-changes-for-windows-vista.md).

 

 
