---
description: La propiedad MSIRESTARTMANAGERCONTROL especifica si el paquete de Windows Installer usa la funcionalidad del cuadro de diálogo Administrador de reinicio o FilesInUse.
ms.assetid: fefff18b-892a-440e-9f57-d23aeb99af74
title: Propiedad MSIRESTARTMANAGERCONTROL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d965f1b814ce2969a6253ba227672c54769791
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671374"
---
# <a name="msirestartmanagercontrol-property"></a>Propiedad MSIRESTARTMANAGERCONTROL

La propiedad **MSIRESTARTMANAGERCONTROL** especifica si el paquete de Windows Installer usa la funcionalidad del [cuadro de diálogo](filesinuse-dialog.md) administrador de [reinicio](../rstmgr/restart-manager-portal.md) o FilesInUse.

## <a name="value"></a>Value



| Value                                                                                        | Significado                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                 | Este es el valor predeterminado si no se establece la propiedad. Windows Installer siempre intenta usar el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) en Windows Vista.<br/>                                                                                                                                                                                                       |
| <dl> <dt>Activa</dt> </dl>         | Deshabilita la interacción del paquete con el [Administrador de reinicio](../rstmgr/restart-manager-portal.md). Windows Installer usa el [cuadro de diálogo FilesInUse](filesinuse-dialog.md). <br/>                                                                                                                                                                                                      |
| <dl> <dt>"DisableShutdown"</dt> </dl> | Windows Installer usa el [cuadro de diálogo FilesInUse](filesinuse-dialog.md). Esta configuración deshabilita los intentos del [Administrador de reinicio](../rstmgr/restart-manager-portal.md) para mitigar los reinicios al instalar un paquete de Windows Installer que no se ha creado para usar el administrador de reinicio. El instalador sigue usando el administrador de reinicio para detectar los archivos que usan las aplicaciones. <br/> |



 

## <a name="remarks"></a>Observaciones

La propiedad **MSIRESTARTMANAGERCONTROL** se omite si el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) no está disponible o está deshabilitado.

El valor de esta propiedad se puede modificar mediante transformaciones o actualizaciones de personalización. Cambiar el valor de esta propiedad a partir de acciones personalizadas no tiene ningún efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima requerida por una versión de Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md)
</dt> <dt>

[No se admite en Windows Installer 3,1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
