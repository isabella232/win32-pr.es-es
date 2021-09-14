---
description: En Windows 2000 y versiones posteriores, el instalador establece la propiedad MsiNTSuiteBackOffice en 1 si están instalados los componentes de Microsoft BackOffice.
ms.assetid: 31493732-3082-4dd9-9a20-21658f53c8c2
title: Propiedad MsiNTSuiteBackOffice
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2d9f2f1d95446c32b4f2addf520f3d5b4dadc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074364"
---
# <a name="msintsuitebackoffice-property"></a>Propiedad MsiNTSuiteBackOffice

En Windows 2000 y versiones posteriores, el instalador establece la propiedad **MsiNTSuiteBackOffice** en 1 si están instalados los componentes de Microsoft BackOffice. El instalador establece esta propiedad en 1 solo si la marca BACKOFFICE de VER \_ SUITE está establecida en la estructura \_ [**OSVERSIONINFOEX.**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) De lo contrario, el instalador no establece esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 
