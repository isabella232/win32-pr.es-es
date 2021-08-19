---
description: En Windows 2000 y versiones posteriores, el instalador establece la propiedad MsiNTSuiteBackOffice en 1 si están instalados los componentes de Microsoft BackOffice.
ms.assetid: 31493732-3082-4dd9-9a20-21658f53c8c2
title: Propiedad MsiNTSuiteBackOffice
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf3c65e1f5d1d528dd35232900a9aef12bdf344d1d2859eef814d1030e6249d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944830"
---
# <a name="msintsuitebackoffice-property"></a>Propiedad MsiNTSuiteBackOffice

En Windows 2000 y versiones posteriores, el instalador establece la propiedad **MsiNTSuiteBackOffice** en 1 si están instalados los componentes de Microsoft BackOffice. El instalador establece esta propiedad en 1 solo si la marca BACKOFFICE de VER \_ SUITE está establecida en la estructura \_ [**OSVERSIONINFOEX.**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) De lo contrario, el instalador no establece esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte Windows [Installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 
