---
description: Si se establece este bit, el cuadro de diálogo llama periódicamente al instalador.
ms.assetid: 7798cb50-72e4-4530-bf06-1927dd963a01
title: Bit de estilo del cuadro de diálogo TrackDiskSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab0cf234071ace41432e20a598b38fb1fc431e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153742"
---
# <a name="trackdiskspace-dialog-style-bit"></a>Bit de estilo del cuadro de diálogo TrackDiskSpace

Si se establece este bit, el cuadro de diálogo llama periódicamente al instalador. Si la propiedad cambia, notifica a los controles en el cuadro de diálogo. Este estilo se puede usar si hay un control en el cuadro de diálogo que indica el espacio en disco. Si el usuario cambia a otra aplicación, agrega o quita archivos o modifica el espacio en disco disponible, puede implementar rápidamente el cambio con este estilo.

Cualquier cuadro de diálogo que dependa de la propiedad [**OutOfDiskSpace**](outofdiskspace.md) para determinar si se debe mostrar un cuadro de diálogo debe establecer el bit de estilo de cuadro de diálogo TrackDiskSpace del cuadro de diálogo para actualizar dinámicamente el espacio en los volúmenes de destino.

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                                |
|---------|-------------|-----------------------------------------|
| 32      | 0x00000020  | **msidbDialogAttributesTrackDiskSpace** |



 

 

 



