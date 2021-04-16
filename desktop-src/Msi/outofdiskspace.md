---
description: El instalador establece la propiedad OutOfDiskSpace en TRUE si algún volumen que sea un destino de la instalación actual no tiene suficiente espacio en disco para alojar la instalación.
ms.assetid: fb1e3be7-12dd-4036-b657-b91b480fca4a
title: Propiedad OutOfDiskSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a438661e931547b0025f2bf85a2ccc03899f5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679526"
---
# <a name="outofdiskspace-property"></a>Propiedad OutOfDiskSpace

El instalador establece la propiedad **OutOfDiskSpace** en true si algún volumen que sea un destino de la instalación actual no tiene suficiente espacio en disco para alojar la instalación. Si todos los volúmenes tienen suficiente espacio, el valor es FALSE. Acciones de resolución de selección use este valor para cancelar una instalación y generar un cuadro de diálogo.

Esta propiedad es válida en cualquier momento después de ejecutar la [acción CostFinalize](costfinalize-action.md) . El estado de la propiedad [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) se actualiza dinámicamente cada vez que se vuelve a calcular el costo total de instalación (por ejemplo, cada vez que se cambia el estado de la instalación de cualquier característica a través del cuadro de diálogo de [selección](selection-dialog.md) ).

## <a name="remarks"></a>Observaciones

Cualquier cuadro de diálogo que dependa de la propiedad **OutOfDiskSpace** para determinar si se debe mostrar un cuadro de diálogo debe establecer el [bit de estilo de cuadro de diálogo TrackDiskSpace](trackdiskspace-dialog-style-bit.md) del cuadro de diálogo para actualizar dinámicamente el espacio en los volúmenes de destino.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




