---
description: El instalador establece el valor de la propiedad MsiRestartManagerSessionKey en la clave de sesión de la sesión de Restart Manager.
ms.assetid: efbf11f2-38ab-4509-aa01-23fa8cfdaa60
title: Propiedad MsiRestartManagerSessionKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489095e0af617c7ae403811f0eab800c5502e3bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169753"
---
# <a name="msirestartmanagersessionkey-property"></a>Propiedad MsiRestartManagerSessionKey

El instalador establece el valor de la **propiedad MsiRestartManagerSessionKey** en la clave de sesión de [la sesión de Restart Manager.](../rstmgr/restart-manager-portal.md) Las acciones personalizadas pueden usar la clave de sesión para unirse a [la sesión de Restart Manager.](../rstmgr/restart-manager-portal.md)

## <a name="remarks"></a>Observaciones

El instalador establece el valor de la propiedad **MsiRestartManagerSessionKey** durante la inicialización y, a continuación, borra el valor durante [la acción InstallValidate.](installvalidate-action.md) Las acciones personalizadas que necesitan el valor de la propiedad **MsiRestartManagerSessionKey** deben ir antes que la acción InstallValidate en la secuencia de acciones.

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

 

 
