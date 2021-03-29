---
description: El instalador establece el valor de la propiedad MsiSystemRebootPending en 1 si hay una operación pendiente para cambiar el nombre de un archivo.
ms.assetid: 8bbbf42e-fb55-4e5d-a574-2c3aaa87a73a
title: Propiedad MsiSystemRebootPending
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec5db7550be3fa27b0ed272ff08d88a4cad915a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680635"
---
# <a name="msisystemrebootpending-property"></a>Propiedad MsiSystemRebootPending

El instalador establece el valor de la propiedad **MsiSystemRebootPending** en 1 si hay una operación pendiente para cambiar el nombre de un archivo.

Los autores de paquetes pueden basar una condición en la [tabla LaunchCondition](launchcondition-table.md) de esta propiedad para evitar la instalación de su paquete en los casos en los que hay una operación pendiente de cambiar el nombre de un archivo. Esto puede realizarse para evitar que se reinicie el sistema operativo causado por el cambio de nombre del archivo. El instalador no establece la propiedad **MsiSystemRebootPending** en todos los casos que requieren un reinicio del sistema.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 4,5 en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Reinicios del sistema](system-reboots.md)
</dt> <dt>

[No se admite en Windows Installer 3,1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




