---
description: En Windows 2000 y versiones posteriores, el instalador establece la propiedad MsiNTSuiteDataCenter en 1 si Windows datacenter Server 2000 está instalado.
ms.assetid: a777e62a-a360-4d8c-b7a6-00d45c17db66
title: Propiedad MsiNTSuiteDataCenter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106b9119885e15b94bf5d8f2cd4b6954d0891d98
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169825"
---
# <a name="msintsuitedatacenter-property"></a>Propiedad MsiNTSuiteDataCenter

En Windows 2000 y versiones posteriores, el instalador establece la propiedad **MsiNTSuiteDataCenter** en 1 si Windows datacenter Server 2000 está instalado. El instalador establece esta propiedad en 1 solo si la marca VER \_ SUITE DATACENTER está establecida en la estructura \_ [**OSVERSIONINFOEX.**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) De lo contrario, el instalador no establece esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 
