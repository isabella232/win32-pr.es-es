---
description: En los sistemas operativos Windows 2000 y posteriores, el instalador establece la propiedad MsiNTSuiteDataCenter en 1 si Windows 2000 Datacenter Server está instalado.
ms.assetid: a777e62a-a360-4d8c-b7a6-00d45c17db66
title: Propiedad MsiNTSuiteDataCenter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106b9119885e15b94bf5d8f2cd4b6954d0891d98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653915"
---
# <a name="msintsuitedatacenter-property"></a>Propiedad MsiNTSuiteDataCenter

En los sistemas operativos Windows 2000 y posteriores, el instalador establece la propiedad **MsiNTSuiteDataCenter** en 1 si Windows 2000 Datacenter Server está instalado. El instalador establece esta propiedad en 1 solo si la \_ marca del \_ centro de centros de recursos de ver conjunto está establecida en la estructura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) . De lo contrario, el instalador no establece esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 
