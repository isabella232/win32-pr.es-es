---
description: Si se establece este bit, el cuadro de diálogo llama periódicamente al instalador.
ms.assetid: 7798cb50-72e4-4530-bf06-1927dd963a01
title: Bit de estilo de diálogo TrackDiskSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8e12a77f0b7e67bd82e094953a2bacd8204d93b444dc6bd1dc378602e67809
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810575"
---
# <a name="trackdiskspace-dialog-style-bit"></a>Bit de estilo de diálogo TrackDiskSpace

Si se establece este bit, el cuadro de diálogo llama periódicamente al instalador. Si la propiedad cambia, notifica a los controles en el cuadro de diálogo. Este estilo se puede usar si hay un control en el cuadro de diálogo que indica espacio en disco. Si el usuario cambia a otra aplicación, agrega o quita archivos o modifica el espacio en disco disponible, puede implementar rápidamente el cambio con este estilo.

Cualquier cuadro de diálogo que dependa de la propiedad [**OutOfDiskSpace**](outofdiskspace.md) para determinar si se debe abrir un diálogo debe establecer el bit de estilo de diálogo TrackDiskSpace para que el diálogo actualice dinámicamente el espacio en los volúmenes de destino.

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                                |
|---------|-------------|-----------------------------------------|
| 32      | 0x00000020  | **msidbDialogAttributesTrackDiskSpace** |



 

 

 



