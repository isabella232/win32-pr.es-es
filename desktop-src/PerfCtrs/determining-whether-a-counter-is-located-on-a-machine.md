---
description: Para determinar si un contador está instalado en un equipo determinado, llame a PdhValidatePath con la ruta de acceso completa del contador. La función devuelve ERROR \_ SUCCESS si el contador se encuentra en el equipo especificado.
ms.assetid: 5533a8d8-3621-4ce7-984c-c3895adef531
title: Determinar si un contador se encuentra en un equipo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2cc6672125f961fc2759d264caa6c33ab68f46347c915e82d1666f667692fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061203"
---
# <a name="determining-whether-a-counter-is-located-on-a-computer"></a>Determinar si un contador se encuentra en un equipo

Para determinar si un contador está instalado en un equipo determinado, llame a [**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) con la ruta de acceso completa del contador. La función devuelve ERROR \_ SUCCESS si el contador se encuentra en el equipo especificado.

[**PdhValidatePath valida**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) toda la ruta de acceso; por lo tanto, si no existe ningún objeto, instancia o contador en la ruta de acceso, el valor devuelto lo indica. **PdhValidatePath comprueba** la ruta de acceso del contador especificada en este orden: equipo, objeto de rendimiento, instancia y contador.

 

 



