---
description: El instalador establece esta propiedad si el usuario tiene privilegios de administrador.
ms.assetid: 2e7fd269-bd5f-40b7-b123-36b9c783a917
title: Propiedad AdminUser
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11651f0d7103edabbcf7b40087db91f999b1a5b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105654006"
---
# <a name="adminuser-property"></a>Propiedad AdminUser

El instalador establece esta propiedad si el usuario tiene privilegios de administrador.

**Windows Server 2008 y Windows Vista:** La propiedad **AdminUser** es la misma que la propiedad [**privileged**](privileged.md) . Los autores deben usar la propiedad **privileged** . El instalador establece estas propiedades si el usuario tiene privilegios de administrador, si la aplicación ha sido asignada por un administrador del sistema, o si las directivas de usuario y de equipo AlwaysInstallElevated están establecidas en true.

## <a name="remarks"></a>Observaciones

Las diferencias entre estas propiedades se pueden haber usado en algunos paquetes heredados. Por ejemplo, se puede haber utilizado **AdminUser** en lugar de [**privileged**](privileged.md) en instrucciones condicionales, porque el instalador solo establece la propiedad **AdminUser** si el usuario es un administrador. El instalador establece la propiedad **privileged** si el usuario es un administrador o si la Directiva permite al usuario instalar con privilegios elevados.

**Windows Server 2008 y Windows Vista:** No compatible. [**Privileged**](privileged.md) y **AdminUser** son los mismos. Los paquetes que requieren distintas propiedades **privileged** y **AdminUser** pueden restaurar la diferencia estableciendo la propiedad [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md) .

Para obtener más información, vea [instalar un paquete con privilegios elevados para una propiedad sin privilegios de administrador](installing-a-package-with-elevated-privileges-for-a-non-admin.md)y con [**privilegios**](privileged.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Vista o Windows Server 2008. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




