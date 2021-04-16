---
description: La propiedad MSIRMSHUTDOWN determina cómo se deben cerrar las aplicaciones o servicios que usan actualmente los archivos afectados por una actualización para habilitar la instalación de la actualización.
ms.assetid: 6763a490-8d1a-42d2-a8cb-0743b7ba6866
title: Propiedad MSIRMSHUTDOWN
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4011e4fad980913271012dd86de44eec8c514f7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671372"
---
# <a name="msirmshutdown-property"></a>Propiedad MSIRMSHUTDOWN

La propiedad **MSIRMSHUTDOWN** determina cómo se deben cerrar las aplicaciones o servicios que usan actualmente los archivos afectados por una actualización para habilitar la instalación de la actualización.

## <a name="value"></a>Value



| Value                                                                        | Significado                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Los procesos o servicios que usan actualmente los archivos afectados por la actualización se apagan.<br/>                                                                                                                                                                   |
| <dl> <dt>1</dt> </dl> | Los procesos o servicios que usan actualmente los archivos afectados por la actualización y que no responden al [Administrador de reinicio](../rstmgr/restart-manager-portal.md), están obligados a cerrarse.<br/>                                                                                       |
| <dl> <dt>2</dt> </dl> | Los procesos o servicios que usan actualmente archivos afectados por la actualización solo se apagan si se han registrado para un reinicio. Si algún proceso o servicio no se ha registrado para un reinicio, no se cerrarán los procesos ni los servicios.<br/> |



 

## <a name="remarks"></a>Observaciones

La propiedad **MSIRMSHUTDOWN** se omite si el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) no está disponible o está deshabilitado.

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

 

 
