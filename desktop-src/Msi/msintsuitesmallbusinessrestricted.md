---
description: En Windows 2000 y versiones posteriores, el instalador establece la propiedad MsiNTSuiteSmallBusinessRestricted en 1 si Microsoft Small Business Server está instalado con la licencia de cliente restrictiva en vigor.
ms.assetid: a7100df4-6fe4-4159-ba94-9b5bd1803107
title: Propiedad MsiNTSuiteSmallBusinessRestricted
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d85fa7fe83c0c8c7cd40788453d1078e7a6b94
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169806"
---
# <a name="msintsuitesmallbusinessrestricted-property"></a>Propiedad MsiNTSuiteSmallBusinessRestricted

En Windows 2000 y versiones posteriores, el instalador establece la propiedad **MsiNTSuiteSmallBusinessRestricted** en 1 si Microsoft Small Business Server está instalado con la licencia de cliente restrictiva en vigor. El instalador establece esta propiedad en 1 solo si la marca VER SUITE SMALLBUSINESS RESTRICTED está establecida en la \_ \_ estructura \_ [**OSVERSIONINFOEX.**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) De lo contrario, el instalador no establece esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 
