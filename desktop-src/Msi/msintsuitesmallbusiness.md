---
description: En Windows 2000 y versiones posteriores, el instalador establece la propiedad MsiNTSuiteSmallBusiness en 1 si microsoft Small Business Server está instalado.
ms.assetid: 9ac578b9-316f-413c-aae0-4f414109583b
title: Propiedad MsiNTSuiteSmallBusiness
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d8b1e523ff038e4639cb0f92762c3914bbf5f6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169809"
---
# <a name="msintsuitesmallbusiness-property"></a>Propiedad MsiNTSuiteSmallBusiness

En Windows 2000 y versiones posteriores, el instalador establece la propiedad **MsiNTSuiteSmallBusiness** en 1 si está instalado Microsoft Small Business Server. El instalador establece esta propiedad en 1 solo si la marca VER \_ SUITE \_ SMALLBUSINESS está establecida en la [**estructura OSVERSIONINFOEX.**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) De lo contrario, el instalador no establece esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 
