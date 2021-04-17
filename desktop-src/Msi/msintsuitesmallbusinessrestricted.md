---
description: En los sistemas operativos Windows 2000 y posteriores, el instalador establece la propiedad MsiNTSuiteSmallBusinessRestricted en 1 si Microsoft Small Business Server se instala con la licencia de cliente restrictiva en vigor.
ms.assetid: a7100df4-6fe4-4159-ba94-9b5bd1803107
title: Propiedad MsiNTSuiteSmallBusinessRestricted
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d85fa7fe83c0c8c7cd40788453d1078e7a6b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653552"
---
# <a name="msintsuitesmallbusinessrestricted-property"></a>Propiedad MsiNTSuiteSmallBusinessRestricted

En los sistemas operativos Windows 2000 y posteriores, el instalador establece la propiedad **MsiNTSuiteSmallBusinessRestricted** en 1 si Microsoft Small Business Server se instala con la licencia de cliente restrictiva en vigor. El instalador establece esta propiedad en 1 solo si la \_ marca ver \_ conjunto \_ de SMALLBUSINESS restringido está establecida en la estructura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) . En caso contrario, el instalador no establece esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 
