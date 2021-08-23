---
description: La propiedad MSIRMSHUTDOWN determina cómo se deben apagar las aplicaciones o servicios que usan actualmente archivos afectados por una actualización para habilitar la instalación de la actualización.
ms.assetid: 6763a490-8d1a-42d2-a8cb-0743b7ba6866
title: Propiedad MSIRMSHUTDOWN
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac31a924727217ac86937f4f7ac553717138461e0668a7e79916ffab796f8bd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012883"
---
# <a name="msirmshutdown-property"></a>Propiedad MSIRMSHUTDOWN

La **propiedad MSIRMSHUTDOWN** determina cómo se deben apagar las aplicaciones o servicios que usan actualmente archivos afectados por una actualización para habilitar la instalación de la actualización.

## <a name="value"></a>Value



| Value                                                                        | Significado                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Los procesos o servicios que usan actualmente archivos afectados por la actualización se cierran.<br/>                                                                                                                                                                   |
| <dl> <dt>1</dt> </dl> | Los procesos o servicios que actualmente usan archivos afectados por la actualización y que no responden al Administrador de reinicio [se](../rstmgr/restart-manager-portal.md)ven obligados a cerrarse.<br/>                                                                                       |
| <dl> <dt>2</dt> </dl> | Los procesos o servicios que actualmente usan archivos afectados por la actualización se cierran solo si todos se han registrado para un reinicio. Si no se ha registrado ningún proceso o servicio para un reinicio, no se cierra ningún proceso o servicio.<br/> |



 

## <a name="remarks"></a>Comentarios

La **propiedad MSIRMSHUTDOWN** se omite si [el Administrador de reinicio](../rstmgr/restart-manager-portal.md) no está disponible o deshabilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre el Service Pack mínimo requerido por una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[No se admite en Windows Installer 3.1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
