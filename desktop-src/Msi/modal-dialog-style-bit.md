---
description: Si se establece este bit, el cuadro de diálogo es modal, no se pueden colocar otros cuadros de diálogo de la misma aplicación y el cuadro de diálogo mantiene el control mientras se está ejecutando.
ms.assetid: 14871dc7-c928-4381-a043-6beb06d25214
title: Bit de estilo del cuadro de diálogo modal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd0004cc7b31557f9a606050a1f8569fa2a493d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546358"
---
# <a name="modal-dialog-style-bit"></a>Bit de estilo del cuadro de diálogo modal

Si se establece este bit, el cuadro de diálogo es modal, no se pueden colocar otros cuadros de diálogo de la misma aplicación y el cuadro de diálogo mantiene el control mientras se está ejecutando. Si no se establece este bit, el cuadro de diálogo es un modelo no modal; puede que otros cuadros de diálogo de la misma aplicación se muevan por encima. Después de crear y mostrar un cuadro de diálogo no modal, la interfaz de usuario devuelve el control al instalador. Después, el instalador llama a la interfaz de usuario periódicamente para actualizar el cuadro de diálogo y darle la oportunidad de procesar los mensajes. En cuanto esto se hace, el control se devuelve al instalador.

> [!Note]  
> No debería haber ningún cuadro de diálogo no modal en una secuencia del asistente, ya que esto devolvería el control al instalador, finalizando la secuencia del asistente prematuramente.

 

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                          |
|---------|-------------|-----------------------------------|
| 2       | 0x00000002  | **msidbDialogAttributesSysModal** |



 

 

 



