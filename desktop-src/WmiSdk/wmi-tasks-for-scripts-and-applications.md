---
description: Describe cómo buscar la clase y los procedimientos de WMI correctos para usar en scripts y aplicaciones que realizan tareas comunes de administración de equipos y redes.
ms.assetid: fe15b67c-8ae6-4360-a2ee-1eda292dd05a
ms.tgt_platform: multiple
title: Tareas de WMI para scripts y aplicaciones
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e2a18791f5055a7574b9e130cf10c0cd1246f6eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544822"
---
# <a name="wmi-tasks-for-scripts-and-applications"></a>Tareas de WMI para scripts y aplicaciones

En las secciones siguientes se describen diversas tareas de administración de equipos y redes y se proporcionan vínculos a la clase o clases WMI utilizadas para realizar dichas tareas. Para obtener más información, vea [crear una aplicación o un script WMI](creating-a-wmi-application-or-script.md). Para obtener más información sobre el uso de WMI, vea [más información](further-information.md). Para obtener más información acerca del uso de WMI, consulte [technet ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx). (Es posible que estos recursos no estén disponibles en todos los idiomas o países o regiones).

Para obtener más información acerca de cómo proporcionar datos a WMI, vea [usar WMI](using-wmi.md), que hará referencia a temas sobre la escritura de un [*proveedor*](gloss-p.md)de WMI.

Las operaciones que se muestran en los ejemplos de script pueden realizarse en las aplicaciones de C++ o Visual Basic. Para obtener más información, vea [crear una aplicación WMI con c++](creating-a-wmi-application-using-c-.md) y [ejemplos de aplicaciones de c++ de WMI](wmi-c---application-examples.md).

En la tabla siguiente se enumeran las categorías de tareas.



| Categorías de tareas                                                               | Descripción                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cuentas y dominios](wmi-tasks--accounts-and-domains.md)                   | Obtener información como el dominio del equipo o el usuario que ha iniciado sesión actualmente. Muchas tareas relacionadas con el dominio o la cuenta se realizan mejor con los scripts [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) . Para obtener ejemplos, vea TechNet ScriptCenter en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) . |
| [Hardware del equipo](wmi-tasks--computer-hardware.md)                         | Obtenga información sobre la presencia, el estado o las propiedades de los componentes de hardware. Por ejemplo, puede determinar si un equipo es un equipo de escritorio o portátil.                                                                                                                                                                                             |
| [Software de equipo](wmi-tasks--computer-software.md)                         | Obtenga información como qué software instala el Windows Installer (MSI) y las versiones de software.                                                                                                                                                                                                                                              |
| [Conexión al servicio WMI](wmi-tasks--connecting-to-the-wmi-service.md) | Para obtener datos de WMI, en el equipo local o desde un equipo remoto, debe conectarse al servicio WMI mediante la conexión a un [*espacio de nombres*](gloss-n.md)específico. En la mayoría de los casos, puede usar la conexión de [moniker](creating-a-wmi-script.md) abreviada o la conexión del [**localizador**](swbemlocator-connectserver.md) .    |
| [Fechas y horas](wmi-tasks--dates-and-times.md)                             | Hay clases WMI y un objeto de scripting para analizar o convertir el formato de [fecha y hora de CIM](date-and-time-format.md) .                                                                                                                                                                                                                                     |
| [Administración de escritorio](wmi-tasks--desktop-management.md)                       | Obtener datos o controlar los escritorios remotos. Por ejemplo, puede determinar si el protector de la contraseña requiere o no una contraseña. WMI también ofrece la posibilidad de apagar un equipo remoto.                                                                                                                                                               |
| [Discos y sistemas de archivos](wmi-tasks--disks-and-file-systems.md)               | Obtenga información sobre el estado del hardware de la unidad de disco, los volúmenes lógicos.                                                                                                                                                                                                                                                                                      |
| [Registros de eventos](wmi-tasks--event-logs.md)                                       | Obtener datos de eventos de archivos de registro de eventos de NT y realizar operaciones como la copia de seguridad o la eliminación de archivos de registro.                                                                                                                                                                                                                                                   |
| [Archivos y carpetas](wmi-tasks--files-and-folders.md)                         | Cambie las propiedades de archivo o carpeta a través de WMI, incluida la creación de un recurso compartido o el cambio de nombre de un archivo.                                                                                                                                                                                                                                                              |
| [Redes](wmi-tasks--networking.md)                                       | Administrar y obtener información acerca de las conexiones y las direcciones IP o MAC.                                                                                                                                                                                                                                                                                  |
| [Sistemas operativos](wmi-tasks--operating-systems.md)                         | Obtenga información sobre el sistema operativo, como la versión, si está activada o qué revisiones están instaladas.                                                                                                                                                                                                                                  |
| [Supervisión del rendimiento](wmi-tasks--performance-monitoring.md)               | Utilice las clases WMI que obtienen datos de contadores de rendimiento para obtener acceso y actualizar datos sobre el rendimiento del equipo.                                                                                                                                                                                                                                     |
| [Procesos](wmi-tasks--processes.md)                                         | Obtenga información como la cuenta con la que se ejecuta un proceso. Puede realizar acciones como la creación de procesos.                                                                                                                                                                                                                                 |
| [Impresoras e impresión](wmi-tasks--printers-and-printing.md)                 | Administrar y obtener datos acerca de las impresoras, como buscar o establecer la impresora predeterminada.                                                                                                                                                                                                                                                                    |
| [Registro](wmi-tasks--registry.md)                                           | Crear y modificar claves y valores del registro.                                                                                                                                                                                                                                                                                                               |
| [Tareas programadas](wmi-tasks--scheduled-tasks.md)                             | Crear y obtener información acerca de las tareas programadas.                                                                                                                                                                                                                                                                                                         |
| [Servicios](wmi-tasks--services.md)                                           | Obtenga información acerca de los servicios, incluidos los servicios dependientes o antecedentes.                                                                                                                                                                                                                                                                            |



 

 

 
