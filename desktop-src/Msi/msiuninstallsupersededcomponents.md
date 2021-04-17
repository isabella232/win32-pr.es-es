---
description: Establezca la propiedad MSIUNINSTALLSUPERSEDEDCOMPONENTS en 1 en la tabla de propiedades o en una línea de comandos.
ms.assetid: ba9b1b2d-1667-48c8-8f1a-9958a1d170da
title: Propiedad MSIUNINSTALLSUPERSEDEDCOMPONENTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc930a258d8faebe71480f466f2b097fe1eda68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680790"
---
# <a name="msiuninstallsupersededcomponents-property"></a>Propiedad MSIUNINSTALLSUPERSEDEDCOMPONENTS

Establezca la propiedad **MSIUNINSTALLSUPERSEDEDCOMPONENTS** en 1 en la [tabla de propiedades](property-table.md) o en una línea de comandos. Cuando esta propiedad se ha establecido en 1, el instalador determina si los componentes de las revisiones reemplazadas se están volviendo redundantes. El instalador puede anular el registro y desinstalar los componentes redundantes para evitar que queden detrás de los componentes huérfanos en el equipo.

El establecimiento de esta propiedad afecta a los componentes de todas las revisiones que se reemplazan. Para habilitar esta funcionalidad para componentes individuales, use el atributo **msidbComponentAttributesUninstallOnSupersedence** en la [tabla de componentes](component-table.md).

**[Windows Installer 4,0 y versiones anteriores](not-supported-in-windows-installer-4-0.md):** No compatible. Las versiones anteriores a Windows Installer 4,5 omiten la propiedad **MSIUNINSTALLSUPERSEDEDCOMPONENTS** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,5 o Windows Installer 4,5 en Windows Vista, Windows XP, Windows Server 2003 y Windows Server 2008. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




