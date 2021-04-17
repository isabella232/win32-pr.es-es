---
description: Si se establece este bit, el cuadro de diálogo es un cuadro de diálogo de error.
ms.assetid: a8a95f6a-6465-433b-98a4-95281cddedd3
title: Bit de estilo del cuadro de diálogo de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ff3e4868cf1941f80be4f7b2d70068ec949a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652483"
---
# <a name="error-dialog-style-bit"></a>Bit de estilo del cuadro de diálogo de error

Si se establece este bit, el cuadro de diálogo es un cuadro de diálogo de error.

Puede haber más de un cuadro de diálogo con este estilo. La propiedad **ErrorDialog** determina qué cuadro de diálogo se usa como cuadro de diálogo de error. El cuadro de diálogo seleccionado solo puede ser uno de los que tienen este bit de estilo establecido. El cuadro de diálogo de error debe tener un control de texto estático denominado ErrorText. Este control recibe el texto del mensaje de error. El cuadro de diálogo también debe tener los siete botones de reenvío correspondientes a los posibles valores devueltos. El mensaje de error determina cuál de estos botones se muestra realmente. Los botones mostrados se reorganizan de modo que se distribuyan uniformemente en el cuadro de diálogo. Esta reorganización cambia la coordenada X de los botones, pero no las otras tres coordenadas. Por lo tanto, es aconsejable que no se cree ningún otro control en la misma región horizontal del cuadro de diálogo que los botones. Si el mensaje de error no especifica ningún botón, se muestra el botón **Aceptar** . El botón **predeterminado** , el primer control activo y los valores del botón **Cancelar** se omiten en un cuadro de diálogo de error. El botón **predeterminado** definido en el mensaje de error se asignará a los tres valores. El efecto de insertar estos botones debe definirse en la [tabla ControlEvent,](controlevent-table.md) como para todos los demás botones. El título del cuadro de diálogo se crea de forma similar a otros cuadros de diálogo. Se puede sobrescribir con el mensaje de error si especifica un texto de encabezado después de la lista de botones.

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                       |
|---------|-------------|--------------------------------|
| 65536   | 0x00010000  | **msidbDialogAttributesError** |



 

 

 



