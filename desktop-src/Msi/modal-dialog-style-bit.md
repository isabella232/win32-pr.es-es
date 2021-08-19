---
description: Si se establece este bit, el cuadro de diálogo es modal, no se pueden colocar otros diálogos de la misma aplicación encima de él y el diálogo mantiene el control mientras se ejecuta.
ms.assetid: 14871dc7-c928-4381-a043-6beb06d25214
title: Bit de estilo de diálogo modal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3663445a81acf07aebd9961f8ddb048dc8c8f466968573ac2c45544d6bd79baa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945482"
---
# <a name="modal-dialog-style-bit"></a>Bit de estilo de diálogo modal

Si se establece este bit, el cuadro de diálogo es modal, no se pueden colocar otros diálogos de la misma aplicación encima de él y el diálogo mantiene el control mientras se ejecuta. Si no se establece este bit, el diálogo es modeless y otros diálogos de la misma aplicación se pueden mover encima de él. Después de crear y mostrar un cuadro de diálogo de modelado, la interfaz de usuario devuelve el control al instalador. A continuación, el instalador llama a la interfaz de usuario periódicamente para actualizar el cuadro de diálogo y darle la oportunidad de procesar los mensajes. En cuanto esto se hace, el control se devuelve al instalador.

> [!Note]  
> No debería haber diálogos de modelado en una secuencia del asistente, ya que esto devolvería el control al instalador, finalizando la secuencia del asistente prematuramente.

 

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                          |
|---------|-------------|-----------------------------------|
| 2       | 0x00000002  | **msidbDialogAttributesSysModal** |



 

 

 



