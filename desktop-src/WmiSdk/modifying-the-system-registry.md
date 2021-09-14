---
description: El registro del sistema contiene datos de configuración que usan el sistema operativo, los servicios y las aplicaciones.
ms.assetid: e16a5d4c-46a0-4798-894d-0af4cfa18f22
ms.tgt_platform: multiple
title: Modificar el Registro del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb274163999996267b5f1df62fb9352831763d4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070453"
---
# <a name="modifying-the-system-registry"></a>Modificar el Registro del sistema

El registro del sistema contiene datos de configuración que usan el sistema operativo, los servicios y las aplicaciones. Windows Instrumental de administración (WMI) tiene un proveedor del Registro del sistema y la clase [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) con métodos que usan para supervisar o modificar el Registro en el equipo local o equipos remotos. [](/previous-versions/windows/desktop/regprov/system-registry-provider) El [proveedor win32 admite](/windows/desktop/CIMWin32Prov/win32-provider) la clase Del [**\_ Registro win32**](/windows/desktop/CIMWin32Prov/win32-registry) que contiene datos estáticos sobre el tamaño de un registro.

El proveedor del Registro del sistema es una instancia, propiedad y proveedor de eventos que se interfaces con el registro del sistema. El proveedor del Registro del sistema es un proveedor estándar con la [**interfaz IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) Puede usar el proveedor del Registro del sistema para acceder a las claves del Registro y a la información de los sistemas locales y remotos. Para obtener más información, vea [Proveedor del Registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider).

WMI coloca [**StdRegProv en el**](/previous-versions/windows/desktop/regprov/stdregprov) espacio de nombres predeterminado \\ raíz. Sin embargo, puede compilar el archivo Regevent.mof en otros espacios de nombres para que lo usen otras aplicaciones.

Los temas identificados en la tabla siguiente pueden mostrar cómo usar la [**clase StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) y el proveedor del Registro del sistema.



| Tema                                                                                              | Descripción                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Obtener datos del Registro](obtaining-registry-data.md)                                             | Puede obtener o modificar datos del Registro a través de métodos de la clase [**StdRegProv,**](/previous-versions/windows/desktop/regprov/stdregprov) que le permite automatizar las actividades del Registro de forma local o remota.                    |
| [Cambio de los datos del Registro](changing-registry-data.md)                                               | Puede agregar o eliminar claves y agregar o cambiar los valores de entrada del Registro en claves.                                                                                                                    |
| [Programación con el proveedor del Registro del sistema](programming-with-the-system-registry-provider.md) | Puede definir sus propias clases que el Registro del sistema proporciona con datos.                                                                                                                       |
| [Registro de eventos del Registro del sistema](registering-for-system-registry-events.md)               | El proveedor del Registro del sistema puede enviar eventos a un consumidor. Para recibir eventos, debe registrar el consumidor, crear una consulta y, a continuación, asegurarse de que el proveedor le envía eventos correctamente. |
| [Registro del proveedor del Registro del sistema](registering-the-system-registry-provider.md)           | El proveedor del Registro del sistema se registra como parte del proceso de instalación de WMI.                                                                                                                |



 

 

 
