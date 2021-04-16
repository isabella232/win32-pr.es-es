---
description: El instalador establece el valor de la propiedad MsiRestartManagerSessionKey en la clave de sesión para la sesión del administrador de reinicio.
ms.assetid: efbf11f2-38ab-4509-aa01-23fa8cfdaa60
title: Propiedad MsiRestartManagerSessionKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489095e0af617c7ae403811f0eab800c5502e3bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671373"
---
# <a name="msirestartmanagersessionkey-property"></a>Propiedad MsiRestartManagerSessionKey

El instalador establece el valor de la propiedad **MsiRestartManagerSessionKey** en la clave de sesión para la sesión del [Administrador de reinicio](../rstmgr/restart-manager-portal.md) . Las acciones personalizadas pueden usar la clave de sesión para unirse a la sesión del [Administrador de reinicio](../rstmgr/restart-manager-portal.md) .

## <a name="remarks"></a>Observaciones

El instalador establece el valor de la propiedad **MsiRestartManagerSessionKey** en la inicialización y, a continuación, borra el valor durante la acción [InstallValidate](installvalidate-action.md) . Las acciones personalizadas que necesitan el valor de la propiedad **MsiRestartManagerSessionKey** deben ir antes de la acción InstallValidate en la secuencia de acción.

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

 

 
