---
description: El instalador establece la propiedad OutOfDiskSpace en TRUE si algún volumen que sea un destino de la instalación actual no tiene suficiente espacio en disco para dar cabida a la instalación.
ms.assetid: fb1e3be7-12dd-4036-b657-b91b480fca4a
title: Propiedad OutOfDiskSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a438661e931547b0025f2bf85a2ccc03899f5a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250971"
---
# <a name="outofdiskspace-property"></a>Propiedad OutOfDiskSpace

El instalador establece la **propiedad OutOfDiskSpace** en TRUE si algún volumen que sea un destino de la instalación actual no tiene suficiente espacio en disco para dar cabida a la instalación. Si todos los volúmenes tienen espacio suficiente, el valor es FALSE. Las acciones de resolución de selección usan este valor para cancelar una instalación y generar un cuadro de diálogo.

Esta propiedad es válida en cualquier momento después de ejecutar la [acción CostFinalize.](costfinalize-action.md) El estado de la propiedad [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) se actualiza dinámicamente cada vez que se vuelve a calcular el costo total de instalación (por ejemplo, cada vez que se cambia el estado de instalación de cualquier característica a través del cuadro de diálogo [Selección).](selection-dialog.md)

## <a name="remarks"></a>Observaciones

Cualquier diálogo que dependa de la propiedad **OutOfDiskSpace** para determinar si se debe abrir un diálogo debe establecer el bit de estilo de diálogo [TrackDiskSpace](trackdiskspace-dialog-style-bit.md) para que el diálogo actualice dinámicamente el espacio en los volúmenes de destino.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




