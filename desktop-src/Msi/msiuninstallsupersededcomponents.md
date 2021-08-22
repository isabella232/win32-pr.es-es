---
description: Establezca la propiedad MSIUNINSTALLSUPERSEDEDCOMPONENTS en 1 en la tabla Property o en una línea de comandos.
ms.assetid: ba9b1b2d-1667-48c8-8f1a-9958a1d170da
title: Propiedad MSIUNINSTALLSUPERSEDCOMPONENTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae30e142167e2d080fa4c74c046625338fbf92fd4476b0339d60f77e321ab54a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943946"
---
# <a name="msiuninstallsupersededcomponents-property"></a>Propiedad MSIUNINSTALLSUPERSEDCOMPONENTS

Establezca la **propiedad MSIUNINSTALLSUPERSEDEDCOMPONENTS** en 1 en la tabla [Property](property-table.md) o en una línea de comandos. Cuando esta propiedad se ha establecido en 1, el instalador determina si los componentes de las revisiones reemplazadas se están volviendo redundantes. El instalador puede anular el registro y desinstalar los componentes redundantes para evitar quedarse con componentes huérfanos en el equipo.

Establecer esta propiedad afecta a los componentes de todas las revisiones que se sustituyen. Para habilitar esta funcionalidad para componentes únicos, use el atributo **msidbComponentAttributesUninstallOnSupersedence** en la [tabla Component](component-table.md).

**[Windows Installer 4.0 y versiones anteriores:](not-supported-in-windows-installer-4-0.md)** No se admite. Las versiones anteriores a Windows Installer 4.5 omiten la propiedad **MSIUNINSTALLSUPERSEDEDCOMPONENTS.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.5 o Windows Installer 4.5 en Windows Vista, Windows XP, Windows Server 2003 y Windows Server 2008. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




