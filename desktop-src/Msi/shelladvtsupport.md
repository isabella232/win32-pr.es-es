---
description: El instalador establece la propiedad ShellAdvtSupport si la interfaz IShellLink del sistema admite la resolución del descriptor del instalador.
ms.assetid: 8c3503c5-2a9c-43ad-8cc5-ea10df39b24d
title: Propiedad ShellAdvtSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfacc34bfffdde9ce34841030f38c443a243c9923cb70749a27615cccc1c676e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628445"
---
# <a name="shelladvtsupport-property"></a>Propiedad ShellAdvtSupport

El instalador establece la propiedad **ShellAdvtSupport** si la interfaz [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) del sistema admite la resolución del descriptor del instalador.

## <a name="remarks"></a>Comentarios

Si se establece esta propiedad, la interfaz [**IShellLink del**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) sistema admite la resolución del descriptor del instalador. Esto es compatible con Windows 2000 y sistemas que ejecutan Internet Explorer 4.01. Si no se establece esta propiedad, el instalador tiene el comportamiento predeterminado de crear características no anunciadas durante la instalación, ya sea localmente o desde el origen.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Compatibilidad de la plataforma con anuncios](platform-support-of-advertisement.md)
</dt> </dl>

 

 
