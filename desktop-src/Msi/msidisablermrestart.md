---
description: La propiedad MSIDISABLERMRESTART determina cómo se deben apagar y reiniciar las aplicaciones o servicios que usan actualmente los archivos afectados por una actualización para habilitar la instalación de la actualización.
ms.assetid: 45c804bf-6d15-416a-b106-d8bb3f4c547d
title: Propiedad MSIDISABLERMRESTART
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1215822b26bb9bd48fa52ee46806bc288a2986b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653741"
---
# <a name="msidisablermrestart-property"></a>Propiedad MSIDISABLERMRESTART

La propiedad **MSIDISABLERMRESTART** determina cómo se deben apagar y reiniciar las aplicaciones o servicios que usan actualmente los archivos afectados por una actualización para habilitar la instalación de la actualización.

## <a name="value"></a>Value



| Value                                                                        | Significado                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Se reinician todos los servicios del sistema que se cerraron para instalar la actualización. Se reinician todas las aplicaciones que se registraron con el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) .<br/> |
| <dl> <dt>1</dt> </dl> | Los procesos que se cerraron con el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) al instalar la actualización no se reiniciarán una vez aplicada la actualización.<br/>                           |



 

## <a name="remarks"></a>Observaciones

La propiedad **MSIDISABLERMRESTART** se omite si el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) no está disponible o está deshabilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima requerida por una versión de Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[No se admite en Windows Installer 3,1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
