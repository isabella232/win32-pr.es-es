---
description: La propiedad Privileged indica si la instalación se realiza en el contexto de privilegios elevados.
ms.assetid: 483ab73a-3ff7-4111-a6b5-eac990d85bd7
title: Propiedad con privilegios
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfe61f17e5ef3453021c98bac8eb383171a678adfb204886ecdaa840e0df832
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129135"
---
# <a name="privileged-property"></a>Propiedad con privilegios

La **propiedad Privileged** indica si la instalación se realiza en el contexto de privilegios elevados. El instalador establece esta propiedad si el usuario tiene privilegios de administrador, si un administrador del sistema ha asignado la aplicación o si las directivas de usuario y equipo AlwaysInstallElevated están establecidas en true.

## <a name="default-value"></a>Valor predeterminado

El instalador no establece esta propiedad si el usuario no puede instalar con privilegios elevados.

## <a name="remarks"></a>Comentarios

Los desarrolladores de paquetes del instalador pueden usar la propiedad **Privileged** para que la instalación sea condicional a la directiva del sistema, al usuario como administrador o a la asignación por parte de un administrador.

Cuando se ejecuta Windows Vista, **Privileged** y [**AdminUser**](adminuser.md) son los mismos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




