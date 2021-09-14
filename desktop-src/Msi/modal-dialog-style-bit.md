---
description: Si se establece este bit, el cuadro de diálogo es modal, no se pueden colocar otros diálogos de la misma aplicación sobre él y el diálogo mantiene el control mientras se ejecuta.
ms.assetid: 14871dc7-c928-4381-a043-6beb06d25214
title: Bit de estilo de diálogo modal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd0004cc7b31557f9a606050a1f8569fa2a493d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261231"
---
# <a name="modal-dialog-style-bit"></a>Bit de estilo de diálogo modal

Si se establece este bit, el cuadro de diálogo es modal, no se pueden colocar otros diálogos de la misma aplicación sobre él y el diálogo mantiene el control mientras se ejecuta. Si no se establece este bit, el diálogo es modela y otros diálogos de la misma aplicación se pueden mover encima de él. Después de crear y mostrar un cuadro de diálogo de modelado, la interfaz de usuario devuelve el control al instalador. A continuación, el instalador llama a la interfaz de usuario periódicamente para actualizar el cuadro de diálogo y darle la oportunidad de procesar los mensajes. En cuanto esto se hace, el control se devuelve al instalador.

> [!Note]  
> No debería haber diálogos modelados en una secuencia del asistente, ya que esto devolvería el control al instalador, finalizando la secuencia del asistente prematuramente.

 

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                          |
|---------|-------------|-----------------------------------|
| 2       | 0x00000002  | **msidbDialogAttributesSysModal** |



 

 

 



