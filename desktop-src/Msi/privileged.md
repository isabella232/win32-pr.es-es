---
description: La propiedad privileged indica si la instalación se realiza en el contexto de privilegios elevados.
ms.assetid: 483ab73a-3ff7-4111-a6b5-eac990d85bd7
title: Propiedad privileged
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d28a7079e7ab12b9832447172f1b3b2c8650a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653933"
---
# <a name="privileged-property"></a>Propiedad privileged

La propiedad **privileged** indica si la instalación se realiza en el contexto de privilegios elevados. El instalador establece esta propiedad si el usuario tiene privilegios de administrador, si el administrador del sistema ha asignado la aplicación, o si las directivas de usuario y de equipo AlwaysInstallElevated están establecidas en true.

## <a name="default-value"></a>Valor predeterminado

El instalador no establece esta propiedad si el usuario no tiene permiso para instalar con privilegios elevados.

## <a name="remarks"></a>Observaciones

Los desarrolladores de paquetes del instalador pueden utilizar la propiedad **privileged** para hacer que la instalación sea condicional en la Directiva del sistema, el usuario es un administrador o la asignación por parte de un administrador.

Cuando se ejecuta en Windows Vista, **privileged** y [**AdminUser**](adminuser.md) son los mismos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




