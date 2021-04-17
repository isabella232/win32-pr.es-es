---
description: En Windows XP y sistemas operativos posteriores, el instalador establece la propiedad MsiNTSuitePersonal en 1 si el sistema operativo es Windows XP Home Edition.
ms.assetid: 324a4c45-bd64-4361-90ba-6a0554a9c5ef
title: Propiedad MsiNTSuitePersonal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e8932cf2d2c9c5079d6955571512cbc9836e41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653554"
---
# <a name="msintsuitepersonal-property"></a>Propiedad MsiNTSuitePersonal

En Windows XP y sistemas operativos posteriores, el instalador establece la propiedad **MsiNTSuitePersonal** en 1 si el sistema operativo es Windows XP Home Edition. El instalador establece esta propiedad en 1 solo si \_ \_ se establece la marca personal de ver conjunto en la estructura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) . En caso contrario, el instalador no establece esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 
