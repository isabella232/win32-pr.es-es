---
description: Para determinar si un contador está instalado en un equipo determinado, llame a PdhValidatePath con la ruta de acceso completa del contador. La función devuelve el ERROR \_ Success si el contador se encuentra en el equipo especificado.
ms.assetid: 5533a8d8-3621-4ce7-984c-c3895adef531
title: Determinar si un contador se encuentra en un equipo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 795878e2f9c97989fe924737ec7f8e7f14bdc67c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001979"
---
# <a name="determining-whether-a-counter-is-located-on-a-computer"></a>Determinar si un contador se encuentra en un equipo

Para determinar si un contador está instalado en un equipo determinado, llame a [**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) con la ruta de acceso completa del contador. La función devuelve el ERROR \_ Success si el contador se encuentra en el equipo especificado.

[**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) valida la ruta de acceso completa; por lo tanto, si algún objeto, instancia o contador de la ruta de acceso no existe, el valor devuelto indica esto. **PdhValidatePath** comprueba la ruta de acceso de contador especificada en este orden: equipo, objeto de rendimiento, instancia y contador.

 

 



