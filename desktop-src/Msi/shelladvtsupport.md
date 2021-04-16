---
description: El instalador establece la propiedad ShellAdvtSupport si la interfaz IShellLink del sistema admite la resolución de descriptores de instalador.
ms.assetid: 8c3503c5-2a9c-43ad-8cc5-ea10df39b24d
title: Propiedad ShellAdvtSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0040aef3b53352a9da8a31bf97f14e8df3791e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678941"
---
# <a name="shelladvtsupport-property"></a>Propiedad ShellAdvtSupport

El instalador establece la propiedad **ShellAdvtSupport** si la interfaz [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) del sistema admite la resolución de descriptores de instalador.

## <a name="remarks"></a>Observaciones

Si se establece esta propiedad, la interfaz [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) del sistema admite la resolución de descriptores de instalador. Es compatible con Windows 2000 y los sistemas que ejecutan Internet Explorer 4,01. Si no se establece esta propiedad, el instalador tiene el comportamiento predeterminado de la creación de características no anunciadas durante la instalación, ya sea de forma local o se ejecuta desde el origen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Compatibilidad de la plataforma con el anuncio](platform-support-of-advertisement.md)
</dt> </dl>

 

 
