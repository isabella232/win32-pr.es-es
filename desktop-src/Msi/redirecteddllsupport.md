---
description: El instalador establece la propiedad RedirectedDLLSupport si la plataforma del sistema que realiza la instalación admite componentes aislados.
ms.assetid: 703489c4-cac4-442c-bd96-d3927491a864
title: Propiedad RedirectedDLLSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed308eaf022ada5c6c8697ba47f55605f1fecbd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069708"
---
# <a name="redirecteddllsupport-property"></a>Propiedad RedirectedDLLSupport

El instalador establece la propiedad **RedirectedDLLSupport si** la plataforma del sistema que realiza la instalación admite [componentes aislados](isolated-components.md).

El instalador establece la **propiedad RedirectedDLLSupport** en un valor de 1 si el sistema que realiza la instalación admite [componentes aislados](isolated-components.md) basados en . Archivos LOCALES. El instalador establece la **propiedad RedirectedDLLSupport** en un valor de 2 si el sistema que realiza la instalación admite el aislamiento mediante . Archivos LOCALES o ensamblados en paralelo de Win32.

La **propiedad RedirectedDLLSupport** se puede usar para condición de la acción [IsolateComponents](isolatecomponents-action.md) en la [tabla InstallUISequence](installuisequence-table.md) o en la [tabla InstallExecuteSequence](installexecutesequence-table.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




