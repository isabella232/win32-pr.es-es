---
description: El instalador establece la propiedad OutOfNoRbDiskSpace en true si algún volumen que sea un destino de la instalación no tiene suficiente espacio en disco para alojar la instalación.
ms.assetid: 910d6c1d-38d3-4680-b256-2bf30689ce11
title: Propiedad OutOfNoRbDiskSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fa9cdd7c1d444e141103ca148344dd26ea1d2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653799"
---
# <a name="outofnorbdiskspace-property"></a>Propiedad OutOfNoRbDiskSpace

El instalador establece la propiedad **OutOfNoRbDiskSpace** en true si algún volumen que sea un destino de la instalación no tiene suficiente espacio en disco para alojar la instalación. En este caso, la propiedad **OutOfNoRbDiskSpace** se establece en true incluso si se ha deshabilitado la reversión. Si todos los volúmenes tienen suficiente espacio, el valor es false.

Un desarrollador de un paquete de instalación puede controlar la situación en la que la propiedad [**OutOfDiskSpace**](outofdiskspace.md) es true y la propiedad **OutOfNoRbDiskSpace** es falsa mediante la creación de una interfaz de usuario que presenta al usuario una opción para deshabilitar la reversión y continuar con la instalación. Para obtener información sobre cómo mostrar un cuadro de diálogo condicionalmente, consulte [información general de ControlEvent,](controlevent-overview.md). Para obtener información sobre cómo deshabilitar la reversión, vea [EnableRollback ControlEvent,](enablerollback-controlevent.md).

La propiedad **OutOfNoRbDiskSpace** es válida en cualquier momento después de ejecutar la [acción CostFinalize](costfinalize-action.md) . El estado de la propiedad **OutOfNoRbDiskSpace** se actualiza dinámicamente cada vez que se vuelve a calcular el costo total de instalación (por ejemplo, cada vez que se cambia el estado de la instalación de cualquier característica a través del [cuadro de diálogo de selección](selection-dialog.md)). Acciones de resolución de selección use este valor para cancelar una instalación y generar un cuadro de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Información general de ControlEvent,](controlevent-overview.md)
</dt> <dt>

[**Propiedad OutOfDiskSpace**](outofdiskspace.md)
</dt> <dt>

[EnableRollback ControlEvent,](enablerollback-controlevent.md)
</dt> <dt>

[Acción CostFinalize](costfinalize-action.md)
</dt> <dt>

[Cuadro de diálogo de selección](selection-dialog.md)
</dt> </dl>

 

 




