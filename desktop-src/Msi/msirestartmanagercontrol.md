---
description: La propiedad MSIRESTARTMANAGERCONTROL especifica si el paquete Windows Installer usa la funcionalidad Restart Manager o FilesInUse Dialog.
ms.assetid: fefff18b-892a-440e-9f57-d23aeb99af74
title: Propiedad MSIRESTARTMANAGERCONTROL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912f529187560aa5fffff90407573e5438139d2b2d26345645752c8d30416f60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065965"
---
# <a name="msirestartmanagercontrol-property"></a>Propiedad MSIRESTARTMANAGERCONTROL

La **propiedad MSIRESTARTMANAGERCONTROL** especifica si el paquete Windows Installer usa la funcionalidad Restart [Manager](../rstmgr/restart-manager-portal.md) o [FilesInUse Dialog.](filesinuse-dialog.md)

## <a name="value"></a>Value



| Value                                                                                        | Significado                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                 | Este es el valor predeterminado si no se establece la propiedad . Windows El instalador siempre intenta usar el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) en Windows Vista.<br/>                                                                                                                                                                                                       |
| <dl> <dt>"Deshabilitar"</dt> </dl>         | Deshabilita la interacción del paquete con [el Administrador de reinicio.](../rstmgr/restart-manager-portal.md) Windows El instalador usa el [cuadro de diálogo FilesInUse](filesinuse-dialog.md). <br/>                                                                                                                                                                                                      |
| <dl> <dt>"DisableShutdown"</dt> </dl> | Windows El instalador usa el [cuadro de diálogo FilesInUse](filesinuse-dialog.md). Esta configuración deshabilita los [](../rstmgr/restart-manager-portal.md) intentos del Administrador de reinicio para mitigar los reinicios al instalar un paquete de Windows Installer que no se ha creado para usar el Administrador de reinicio. El instalador sigue utilizando el Administrador de reinicio para detectar archivos en uso por parte de las aplicaciones. <br/> |



 

## <a name="remarks"></a>Comentarios

La **propiedad MSIRESTARTMANAGERCONTROL** se omite si [el Administrador de reinicio](../rstmgr/restart-manager-portal.md) no está disponible o deshabilitado.

El valor de esta propiedad se puede modificar mediante transformaciones o actualizaciones de personalización. Cambiar el valor de esta propiedad a partir de acciones personalizadas no tiene ningún efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre el Service Pack mínimo requerido por una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md)
</dt> <dt>

[No se admite en Windows Installer 3.1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
