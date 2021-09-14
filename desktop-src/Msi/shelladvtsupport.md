---
description: El instalador establece la propiedad ShellAdvtSupport si la interfaz IShellLink del sistema admite la resolución del descriptor del instalador.
ms.assetid: 8c3503c5-2a9c-43ad-8cc5-ea10df39b24d
title: Propiedad ShellAdvtSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0040aef3b53352a9da8a31bf97f14e8df3791e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246374"
---
# <a name="shelladvtsupport-property"></a>Propiedad ShellAdvtSupport

El instalador establece la propiedad **ShellAdvtSupport** si la interfaz [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) del sistema admite la resolución del descriptor del instalador.

## <a name="remarks"></a>Observaciones

Si se establece esta propiedad, la interfaz [**IShellLink del**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) sistema admite la resolución del descriptor del instalador. Esto es compatible con Windows 2000 y sistemas que ejecutan Internet Explorer 4.01. Si no se establece esta propiedad, el instalador tiene el comportamiento predeterminado de crear características no anunciadas durante la instalación, ya sea localmente o desde el origen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Compatibilidad de la plataforma con anuncios](platform-support-of-advertisement.md)
</dt> </dl>

 

 
