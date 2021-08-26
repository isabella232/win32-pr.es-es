---
description: La propiedad MSIDISABLERMRESTART determina cómo se deben apagar y reiniciar las aplicaciones o servicios que usan actualmente archivos afectados por una actualización para habilitar la instalación de la actualización.
ms.assetid: 45c804bf-6d15-416a-b106-d8bb3f4c547d
title: Propiedad MSIDISABLERMRESTART
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d46bdaee34b154ccaacddc36dcb08113fce9e3f749090eb80176080a60235e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042795"
---
# <a name="msidisablermrestart-property"></a>Propiedad MSIDISABLERMRESTART

La **propiedad MSIDISABLERMRESTART** determina cómo se deben apagar y reiniciar las aplicaciones o servicios que usan actualmente archivos afectados por una actualización para habilitar la instalación de la actualización.

## <a name="value"></a>Value



| Value                                                                        | Significado                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Se reinician todos los servicios del sistema que se apagaron para instalar la actualización. Se reinician todas las aplicaciones que se registraron con [el Administrador](../rstmgr/restart-manager-portal.md) de reinicio.<br/> |
| <dl> <dt>1</dt> </dl> | Los procesos que se cerraron mediante [el](../rstmgr/restart-manager-portal.md) Administrador de reinicio durante la instalación de la actualización no se reiniciarán después de aplicar la actualización.<br/>                           |



 

## <a name="remarks"></a>Comentarios

La **propiedad MSIDISABLERMRESTART** se omite si [el Administrador de](../rstmgr/restart-manager-portal.md) reinicio no está disponible o deshabilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre el Service Pack mínimo requerido por una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[No se admite en Windows Installer 3.1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
