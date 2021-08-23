---
description: El instalador establece el valor de la propiedad MsiRestartManagerSessionKey en la clave de sesión de la sesión de Restart Manager.
ms.assetid: efbf11f2-38ab-4509-aa01-23fa8cfdaa60
title: Propiedad MsiRestartManagerSessionKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f48fe8d2ce4b287afc5c222acdc1f71eec393ff9a1ab1773a822e30405e6a317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944543"
---
# <a name="msirestartmanagersessionkey-property"></a>Propiedad MsiRestartManagerSessionKey

El instalador establece el valor de la **propiedad MsiRestartManagerSessionKey** en la clave de sesión de [la sesión de Restart Manager.](../rstmgr/restart-manager-portal.md) Las acciones personalizadas pueden usar la clave de sesión para unirse a [la sesión de Restart Manager.](../rstmgr/restart-manager-portal.md)

## <a name="remarks"></a>Comentarios

El instalador establece el valor de la propiedad **MsiRestartManagerSessionKey** durante la inicialización y, a continuación, borra el valor durante [la acción InstallValidate.](installvalidate-action.md) Las acciones personalizadas que necesitan el valor de la propiedad **MsiRestartManagerSessionKey** deben ir antes que la acción InstallValidate en la secuencia de acciones.

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

 

 
