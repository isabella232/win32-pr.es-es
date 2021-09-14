---
description: Describe cómo buscar la clase WMI y los procedimientos correctos para usarlos en scripts y aplicaciones que realizan tareas comunes de administración de equipos y redes.
ms.assetid: fe15b67c-8ae6-4360-a2ee-1eda292dd05a
ms.tgt_platform: multiple
title: Tareas wmi para scripts y aplicaciones
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e2a18791f5055a7574b9e130cf10c0cd1246f6eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172530"
---
# <a name="wmi-tasks-for-scripts-and-applications"></a>Tareas wmi para scripts y aplicaciones

En las secciones siguientes se describen varias tareas de administración de equipos y redes y se proporcionan vínculos a la clase WMI o a las clases usadas para realizar esas tareas. Para obtener más información, vea [Crear una aplicación WMI o script](creating-a-wmi-application-or-script.md). Para obtener más información sobre el uso de WMI, vea [Información adicional.](further-information.md) Para obtener más información sobre el uso de WMI, [vea TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx). (Es posible que estos recursos no estén disponibles en todos los idiomas, países o regiones).

Para obtener más información sobre cómo proporcionar datos a WMI, vea [Usar WMI](using-wmi.md), que hará referencia a temas sobre cómo escribir un [*proveedor*](gloss-p.md)WMI.

Las operaciones que se muestran en los ejemplos de script pueden realizarse mediante aplicaciones de C++ o Visual Basic. Para obtener más información, vea [Creating a WMI Application Using C++ and](creating-a-wmi-application-using-c-.md) WMI [C++ Application Examples](wmi-c---application-examples.md).

En la tabla siguiente se enumeran las categorías de tareas.



| Categorías de tareas                                                               | Descripción                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cuentas y dominios](wmi-tasks--accounts-and-domains.md)                   | Obtenga información como el dominio del equipo o el usuario que ha iniciado sesión actualmente. Muchas tareas relacionadas con el dominio o la cuenta se realizan mejor con scripts [ADSI.](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Para obtener ejemplos, consulte ScriptCenter de TechNet en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) . |
| [Hardware del equipo](wmi-tasks--computer-hardware.md)                         | Obtenga información sobre la presencia, el estado o las propiedades de los componentes de hardware. Por ejemplo, puede determinar si un equipo es un equipo de escritorio o portátil.                                                                                                                                                                                             |
| [Software de equipo](wmi-tasks--computer-software.md)                         | Obtenga información como qué software instala el instalador de Windows (MSI) y las versiones de software.                                                                                                                                                                                                                                              |
| [Conexión al servicio WMI](wmi-tasks--connecting-to-the-wmi-service.md) | Para obtener datos de WMI, ya sea en el equipo local o desde un equipo remoto, debe conectarse al servicio WMI mediante la conexión a un espacio de nombres [*específico.*](gloss-n.md) En la mayoría de los casos, use la conexión de [moniker](creating-a-wmi-script.md) abreviada o la [**conexión de localizador.**](swbemlocator-connectserver.md)    |
| [Fechas y horas](wmi-tasks--dates-and-times.md)                             | Hay clases WMI y un objeto de scripting para analizar o convertir el formato de fecha y hora [CIM.](date-and-time-format.md)                                                                                                                                                                                                                                     |
| [Administración de escritorio](wmi-tasks--desktop-management.md)                       | Obtener datos de escritorios remotos o controlarlo. Por ejemplo, puede determinar si el protector de pantalla requiere o no una contraseña. WMI también ofrece la posibilidad de apagar un equipo remoto.                                                                                                                                                               |
| [Discos y sistemas de archivos](wmi-tasks--disks-and-file-systems.md)               | Obtenga información sobre el estado de hardware de la unidad de disco, los volúmenes lógicos.                                                                                                                                                                                                                                                                                      |
| [Registros de eventos](wmi-tasks--event-logs.md)                                       | Obtenga datos de eventos de archivos de registro de eventos NT y realice operaciones como realizar una copia de seguridad o borrar archivos de registro.                                                                                                                                                                                                                                                   |
| [Archivos y carpetas](wmi-tasks--files-and-folders.md)                         | Cambie las propiedades de archivo o carpeta a través de WMI, incluida la creación de un recurso compartido o el cambio de nombre de un archivo.                                                                                                                                                                                                                                                              |
| [Redes](wmi-tasks--networking.md)                                       | Administrar y obtener información sobre las conexiones y las direcciones IP o MAC.                                                                                                                                                                                                                                                                                  |
| [Sistemas operativos](wmi-tasks--operating-systems.md)                         | Obtenga información sobre el sistema operativo, como la versión, si está activado o qué revisiones están instaladas.                                                                                                                                                                                                                                  |
| [Supervisión del rendimiento](wmi-tasks--performance-monitoring.md)               | Use las clases WMI que obtienen datos de los contadores de rendimiento para acceder a los datos sobre el rendimiento del equipo y actualizarlo.                                                                                                                                                                                                                                     |
| [Procesos](wmi-tasks--processes.md)                                         | Obtenga información como la cuenta en la que se ejecuta un proceso. Puede realizar acciones como la creación de procesos.                                                                                                                                                                                                                                 |
| [Impresoras e impresión](wmi-tasks--printers-and-printing.md)                 | Administrar y obtener datos sobre impresoras, como buscar o establecer la impresora predeterminada.                                                                                                                                                                                                                                                                    |
| [Registro](wmi-tasks--registry.md)                                           | Crear y modificar claves y valores del Registro.                                                                                                                                                                                                                                                                                                               |
| [Tareas programadas](wmi-tasks--scheduled-tasks.md)                             | Cree y obtenga información sobre las tareas programadas.                                                                                                                                                                                                                                                                                                         |
| [Servicios](wmi-tasks--services.md)                                           | Obtenga información sobre los servicios, incluidos los servicios dependientes o antecedentes.                                                                                                                                                                                                                                                                            |



 

 

 
