---
description: Hay otras circunstancias en las que se puede completar una operación de lectura o escritura con menos del número de caracteres solicitado, aunque no se haya agotado el tiempo de espera.
ms.assetid: 05f84661-34ff-4e1f-9ec8-e4682138dfee
title: Errores de comunicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeace990620928ce898a3e8a31049a0083cdf07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496217"
---
# <a name="communications-errors"></a>Errores de comunicación

Hay otras circunstancias en las que se puede completar una operación de lectura o escritura con menos del número de caracteres solicitado, aunque no se haya agotado el tiempo de espera. A continuación se muestran algunos ejemplos:

-   Algunos controladores admiten el uso de caracteres especiales, que completan una operación de lectura inmediatamente con solo los caracteres que se han leído hasta el momento en que se reciben.
-   Se puede llamar a la función [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) para finalizar prematuramente las operaciones de lectura o escritura pendientes. Esta función también puede eliminar el contenido de los búferes de entrada o de salida, o ambos.
-   Si se produce un error de comunicación durante una operación de lectura o escritura, se terminan todas las operaciones de e/s en el recurso de comunicaciones. Las condiciones de interrupción, los errores de paridad o los errores de trama son ejemplos de estos errores. Cuando se produce un error, el proceso debe llamar a la función [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) para borrar la marca de error antes de poder iniciar operaciones de e/s adicionales. **ClearCommError** informa del error específico que se ha producido y del estado actual del dispositivo.

 

 



