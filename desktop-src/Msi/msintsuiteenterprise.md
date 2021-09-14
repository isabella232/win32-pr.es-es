---
description: En Windows 2000 y versiones posteriores, el instalador establece la propiedad MsiNTSuiteEnterprise en 1 si Windows 2000 Advanced Server está instalado.
ms.assetid: f5384467-3791-4b0b-a70e-b5343c70db46
title: Propiedad MsiNTSuiteEnterprise
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 137b4ece4dbaecdd83b78fd2ce7cfd57820e029d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169821"
---
# <a name="msintsuiteenterprise-property"></a>Propiedad MsiNTSuiteEnterprise

En Windows 2000 y versiones posteriores, el instalador establece la propiedad **MsiNTSuiteEnterprise** en 1 si Windows 2000 Advanced Server está instalado. El instalador establece esta propiedad en 1 solo si la marca VER \_ SUITE ENTERPRISE está establecida en la estructura \_ [**OSVERSIONINFOEX.**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) De lo contrario, el instalador no establece esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 
