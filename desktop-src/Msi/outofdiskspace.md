---
description: El instalador establece la propiedad OutOfDiskSpace en TRUE si algún volumen que sea un destino de la instalación actual no tiene suficiente espacio en disco para dar cabida a la instalación.
ms.assetid: fb1e3be7-12dd-4036-b657-b91b480fca4a
title: OutOfDiskSpace, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a99146d08722038bbc2d9b1e0d7b32fd8b587126b0fc942e14823909a2aef79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042585"
---
# <a name="outofdiskspace-property"></a>OutOfDiskSpace, propiedad

El instalador establece la **propiedad OutOfDiskSpace** en TRUE si algún volumen que sea un destino de la instalación actual no tiene suficiente espacio en disco para dar cabida a la instalación. Si todos los volúmenes tienen espacio suficiente, el valor es FALSE. Las acciones de resolución de selección usan este valor para cancelar una instalación y generar un cuadro de diálogo.

Esta propiedad es válida en cualquier momento después de ejecutar la [acción CostFinalize.](costfinalize-action.md) El estado de la propiedad [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) se actualiza dinámicamente cada vez que se vuelve a calcular el costo total de instalación (por ejemplo, cada vez que se cambia el estado de instalación de cualquier característica a través del cuadro de diálogo [Selección).](selection-dialog.md)

## <a name="remarks"></a>Comentarios

Cualquier diálogo que dependa de la propiedad **OutOfDiskSpace** para determinar si se debe abrir un diálogo debe establecer el bit de estilo de diálogo [TrackDiskSpace](trackdiskspace-dialog-style-bit.md) para que el diálogo actualice dinámicamente el espacio en los volúmenes de destino.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




