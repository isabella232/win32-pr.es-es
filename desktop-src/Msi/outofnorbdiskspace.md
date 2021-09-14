---
description: El instalador establece la propiedad OutOfNoRbDiskSpace en True si cualquier volumen que sea un destino de la instalación no tiene suficiente espacio en disco para dar cabida a la instalación.
ms.assetid: 910d6c1d-38d3-4680-b256-2bf30689ce11
title: Propiedad OutOfNoRbDiskSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fa9cdd7c1d444e141103ca148344dd26ea1d2a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250965"
---
# <a name="outofnorbdiskspace-property"></a>Propiedad OutOfNoRbDiskSpace

El instalador establece la **propiedad OutOfNoRbDiskSpace** en True si cualquier volumen que sea un destino de la instalación no tiene suficiente espacio en disco para dar cabida a la instalación. En este caso, la **propiedad OutOfNoRbDiskSpace** se establece en True incluso si se ha deshabilitado la reversión. Si todos los volúmenes tienen espacio suficiente, el valor es False.

Un desarrollador de un paquete de instalación puede controlar la situación cuando la propiedad [**OutOfDiskSpace**](outofdiskspace.md) es True y la propiedad **OutOfNoRbDiskSpace** es False mediante la creación de una interfaz de usuario que presenta al usuario una opción para deshabilitar la reversión y continuar con la instalación. Para obtener información sobre cómo mostrar condicionalmente un cuadro de diálogo, vea [Información general de ControlEvent.](controlevent-overview.md) Para obtener información sobre cómo deshabilitar la reversión, [vea EnableRollback ControlEvent](enablerollback-controlevent.md).

La **propiedad OutOfNoRbDiskSpace** es válida en cualquier momento después de que se haya ejecutado la acción [CostFinalize.](costfinalize-action.md) El estado de la propiedad **OutOfNoRbDiskSpace** se actualiza dinámicamente cada vez que se vuelve a calcular el costo total de instalación (por ejemplo, cada vez que se cambia el estado de instalación de cualquier característica mediante el cuadro de diálogo [Selección](selection-dialog.md)). Las acciones de resolución de selección usan este valor para cancelar una instalación y generar un cuadro de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Información general de ControlEvent](controlevent-overview.md)
</dt> <dt>

[**Propiedad OutOfDiskSpace**](outofdiskspace.md)
</dt> <dt>

[EnableRollback ControlEvent](enablerollback-controlevent.md)
</dt> <dt>

[Acción CostFinalize](costfinalize-action.md)
</dt> <dt>

[Cuadro de diálogo Selección](selection-dialog.md)
</dt> </dl>

 

 




