---
description: Si se establece este bit, el cuadro de diálogo es un cuadro de diálogo de error.
ms.assetid: a8a95f6a-6465-433b-98a4-95281cddedd3
title: Bit de estilo de cuadro de diálogo de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ff3e4868cf1941f80be4f7b2d70068ec949a4f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158469"
---
# <a name="error-dialog-style-bit"></a>Bit de estilo de cuadro de diálogo de error

Si se establece este bit, el cuadro de diálogo es un cuadro de diálogo de error.

Puede haber más de un diálogo con este estilo. La **propiedad ErrorDialog** determina qué diálogo se usa como diálogo de error. El cuadro de diálogo seleccionado solo puede ser uno de los que tienen este conjunto de bits de estilo. El cuadro de diálogo de error debe tener un control de texto estático denominado ErrorText. Este control recibe el texto del mensaje de error. El cuadro de diálogo también debe tener los siete botones de inserción correspondientes a los posibles valores devueltos. El mensaje de error determina cuál de estos botones se muestra realmente. Los botones mostrados se reorganizan para que se distribuyen uniformemente en el cuadro de diálogo. Esta reorganización cambia la coordenada X de los botones, pero no las otras tres coordenadas. Por lo tanto, es aconsejable que no se cree ningún otro control en la misma región horizontal del cuadro de diálogo que los botones. Si el mensaje de error no especifica ningún botón, se **muestra el** botón Aceptar. Los **valores del botón**  Predeterminado, Primer control activo y Botón Cancelar se omiten para un cuadro de diálogo de error. El **botón** Predeterminado definido en el mensaje de error se asignará a los tres valores. El efecto de insertar estos botones debe definirse en la [tabla ControlEvent](controlevent-table.md) igual que para todos los demás botones. El título del diálogo se ha escrito de forma similar a otros diálogos. El mensaje de error puede sobrescribirlo si especifica un texto de encabezado después de la lista de botones.

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                       |
|---------|-------------|--------------------------------|
| 65536   | 0x00010000  | **msidbDialogAttributesError** |



 

 

 



