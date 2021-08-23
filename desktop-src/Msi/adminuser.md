---
description: El instalador establece esta propiedad si el usuario tiene privilegios de administrador.
ms.assetid: 2e7fd269-bd5f-40b7-b123-36b9c783a917
title: AdminUser, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1b765aa4ece1bc19b5ed59e97a98ca4579042d52d65c0024ae018c794f9aaa3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581915"
---
# <a name="adminuser-property"></a>AdminUser, propiedad

El instalador establece esta propiedad si el usuario tiene privilegios de administrador.

**Windows Server 2008 y Windows Vista:** La **propiedad AdminUser** es la misma que la [**propiedad Privileged.**](privileged.md) Los autores deben usar la **propiedad Privileged.** El instalador establece estas propiedades si el usuario tiene privilegios de administrador, si un administrador del sistema ha asignado la aplicación o si las directivas de usuario y equipo AlwaysInstallElevated están establecidas en true.

## <a name="remarks"></a>Comentarios

Las diferencias entre estas propiedades se pueden haber usado en algunos paquetes heredados. Por ejemplo, **AdminUser se** puede haber usado en lugar de [**Privileged**](privileged.md) en instrucciones condicionales, porque el instalador solo establece la **propiedad AdminUser** si el usuario es administrador. El instalador establece la **propiedad Privileged** si el usuario es administrador o si la directiva permite al usuario instalar con privilegios elevados.

**Windows Server 2008 y Windows Vista:** No se admite. Privileged [**y**](privileged.md) **AdminUser** son los mismos. Los paquetes que requieren propiedades **Privileged** **y AdminUser** distintas pueden restaurar la diferencia estableciendo la [**propiedad MSIUSEREALADMINDETECTION.**](msiuserealadmindetection.md)

Para obtener más información, vea Instalación de un paquete con [privilegios elevados para una](installing-a-package-with-elevated-privileges-for-a-non-admin.md)propiedad que no es de administrador y [**Propiedad con**](privileged.md) privilegios.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Vista o Windows Server 2008. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




