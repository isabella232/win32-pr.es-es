---
description: El instalador establece el valor de la propiedad MsiSystemRebootPending en 1 si hay una operación pendiente para cambiar el nombre de un archivo.
ms.assetid: 8bbbf42e-fb55-4e5d-a574-2c3aaa87a73a
title: Propiedad MsiSystemRebootPending
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec5db7550be3fa27b0ed272ff08d88a4cad915a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161491"
---
# <a name="msisystemrebootpending-property"></a>Propiedad MsiSystemRebootPending

El instalador establece el valor de la **propiedad MsiSystemRebootPending** en 1 si hay una operación pendiente para cambiar el nombre de un archivo.

Los autores de paquetes pueden basar una condición en la [tabla LaunchCondition](launchcondition-table.md) en esta propiedad para evitar la instalación de su paquete en los casos en los que hay una operación pendiente para cambiar el nombre de un archivo. Esto puede hacerse para evitar un reinicio del sistema operativo causado por el cambio de nombre del archivo. El instalador no establece la **propiedad MsiSystemRebootPending** en todos los casos que requieran un reinicio del sistema.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 4.5 en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Reinicios del sistema](system-reboots.md)
</dt> <dt>

[No se admite en Windows Installer 3.1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




