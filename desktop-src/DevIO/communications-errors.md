---
description: Hay otras circunstancias en las que se puede completar una operación de lectura o escritura con menos caracteres que el número solicitado, aunque no se haya producido un tiempo de espera.
ms.assetid: 05f84661-34ff-4e1f-9ec8-e4682138dfee
title: Errores de comunicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeace990620928ce898a3e8a31049a0083cdf07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164522"
---
# <a name="communications-errors"></a>Errores de comunicaciones

Hay otras circunstancias en las que se puede completar una operación de lectura o escritura con menos caracteres que el número solicitado, aunque no se haya producido un tiempo de espera. A continuación se muestran algunos ejemplos:

-   Algunos controladores admiten el uso de caracteres especiales, que completan una operación de lectura inmediatamente con solo los caracteres que se han leído hasta el punto en que se reciben.
-   Se puede llamar a la función [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) para finalizar prematuramente las operaciones de lectura o escritura pendientes. Esta función también puede eliminar el contenido de los búferes de salida o de entrada, o ambos.
-   Si se produce un error de comunicaciones durante una operación de lectura o escritura, se finalizan todas las operaciones de E/S en el recurso de comunicaciones. Las condiciones de interrupción, los errores de paridad o los errores de trama son ejemplos de estos errores. Cuando se produce un error, el proceso debe llamar a la función [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) para borrar la marca de error antes de poder iniciar operaciones de E/S adicionales. **ClearCommError notifica** el error específico que se produjo y el estado actual del dispositivo.

 

 



