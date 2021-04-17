---
description: El registro del sistema contiene datos de configuración que usan el sistema operativo, los servicios y las aplicaciones.
ms.assetid: e16a5d4c-46a0-4798-894d-0af4cfa18f22
ms.tgt_platform: multiple
title: Modificar el registro del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb274163999996267b5f1df62fb9352831763d4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659789"
---
# <a name="modifying-the-system-registry"></a>Modificar el registro del sistema

El registro del sistema contiene datos de configuración que usan el sistema operativo, los servicios y las aplicaciones. Instrumental de administración de Windows (WMI) tiene un [proveedor de registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) y la clase [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) con métodos que usan para supervisar o modificar el registro en el equipo local o en los equipos remotos. El [proveedor Win32](/windows/desktop/CIMWin32Prov/win32-provider) admite la [**clase \_ del registro de Win32**](/windows/desktop/CIMWin32Prov/win32-registry) que contiene datos estáticos sobre el tamaño de un registro.

El proveedor del registro del sistema es una instancia, una propiedad y un proveedor de eventos que interactúa con el registro del sistema. El proveedor del registro del sistema es un proveedor estándar con la interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . Puede usar el proveedor del registro del sistema para tener acceso a las claves del registro y a la información de los sistemas locales y remotos. Para obtener más información, vea [proveedor del registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider).

WMI coloca [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) en el espacio de \\ nombres predeterminado raíz. Sin embargo, puede compilar el archivo Regevent. mof en otros espacios de nombres para que los usen otras aplicaciones.

Los temas que se indican en la tabla siguiente pueden mostrarle cómo usar la clase [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) y el proveedor del registro del sistema.



| Tema                                                                                              | Descripción                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Obtener datos del registro](obtaining-registry-data.md)                                             | Puede obtener o modificar los datos del registro a través de los métodos de la clase [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) , que permite automatizar las actividades del registro de forma local o remota.                    |
| [Cambio de los datos del Registro](changing-registry-data.md)                                               | Puede Agregar o eliminar claves y agregar o cambiar valores de entradas del registro en claves.                                                                                                                    |
| [Programar con el proveedor del registro del sistema](programming-with-the-system-registry-provider.md) | Puede definir sus propias clases que el registro del sistema suministra con los datos.                                                                                                                       |
| [Registrar eventos del registro del sistema](registering-for-system-registry-events.md)               | El proveedor del registro del sistema puede enviar eventos a un consumidor. Para recibir eventos, debe registrar el consumidor, crear una consulta y, a continuación, asegurarse de que el proveedor envía eventos correctamente. |
| [Registrar el proveedor del registro del sistema](registering-the-system-registry-provider.md)           | El proveedor del registro del sistema se registra como parte del proceso de instalación de WMI.                                                                                                                |



 

 

 
