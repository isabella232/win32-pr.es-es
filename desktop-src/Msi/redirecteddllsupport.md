---
description: El instalador establece la propiedad RedirectedDLLSupport si la plataforma del sistema que realiza la instalación admite componentes aislados.
ms.assetid: 703489c4-cac4-442c-bd96-d3927491a864
title: Propiedad RedirectedDLLSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed308eaf022ada5c6c8697ba47f55605f1fecbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670963"
---
# <a name="redirecteddllsupport-property"></a>Propiedad RedirectedDLLSupport

El instalador establece la propiedad **RedirectedDLLSupport** si la plataforma del sistema que realiza la instalación admite [componentes aislados](isolated-components.md).

El instalador establece la propiedad **RedirectedDLLSupport** en un valor de 1 si el sistema que realiza la instalación de admite [componentes aislados](isolated-components.md) basados en. Archivos locales. El instalador establece la propiedad **RedirectedDLLSupport** en un valor de 2 Si el sistema que realiza la instalación admite el aislamiento con cualquiera de las dos. Archivos locales o ensamblados en paralelo de Win32.

La propiedad **RedirectedDLLSupport** se puede usar para condicionar la [acción IsolateComponents](isolatecomponents-action.md) en la tabla [InstallUISequence](installuisequence-table.md) o en la [tabla InstallExecuteSequence](installexecutesequence-table.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




