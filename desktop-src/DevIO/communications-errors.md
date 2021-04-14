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
# <a name="communications-errors"></a><span data-ttu-id="9f56c-103">Errores de comunicación</span><span class="sxs-lookup"><span data-stu-id="9f56c-103">Communications Errors</span></span>

<span data-ttu-id="9f56c-104">Hay otras circunstancias en las que se puede completar una operación de lectura o escritura con menos del número de caracteres solicitado, aunque no se haya agotado el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="9f56c-104">There are other circumstances where a read or write operation can be completed with fewer than the requested number of characters, even though a time-out has not occurred.</span></span> <span data-ttu-id="9f56c-105">A continuación se muestran algunos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="9f56c-105">Following are some examples:</span></span>

-   <span data-ttu-id="9f56c-106">Algunos controladores admiten el uso de caracteres especiales, que completan una operación de lectura inmediatamente con solo los caracteres que se han leído hasta el momento en que se reciben.</span><span class="sxs-lookup"><span data-stu-id="9f56c-106">Some drivers support the use of special characters, which complete a read operation immediately with only the characters that have been read up to the point when they are received.</span></span>
-   <span data-ttu-id="9f56c-107">Se puede llamar a la función [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) para finalizar prematuramente las operaciones de lectura o escritura pendientes.</span><span class="sxs-lookup"><span data-stu-id="9f56c-107">The [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) function can be called to prematurely terminate pending read or write operations.</span></span> <span data-ttu-id="9f56c-108">Esta función también puede eliminar el contenido de los búferes de entrada o de salida, o ambos.</span><span class="sxs-lookup"><span data-stu-id="9f56c-108">This function can also delete the contents of the output or input buffers, or both.</span></span>
-   <span data-ttu-id="9f56c-109">Si se produce un error de comunicación durante una operación de lectura o escritura, se terminan todas las operaciones de e/s en el recurso de comunicaciones.</span><span class="sxs-lookup"><span data-stu-id="9f56c-109">If a communications error occurs during a read or write operation, all I/O operations on the communications resource are terminated.</span></span> <span data-ttu-id="9f56c-110">Las condiciones de interrupción, los errores de paridad o los errores de trama son ejemplos de estos errores.</span><span class="sxs-lookup"><span data-stu-id="9f56c-110">Break conditions, parity errors, or framing errors are examples of such errors.</span></span> <span data-ttu-id="9f56c-111">Cuando se produce un error, el proceso debe llamar a la función [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) para borrar la marca de error antes de poder iniciar operaciones de e/s adicionales.</span><span class="sxs-lookup"><span data-stu-id="9f56c-111">When an error occurs, the process must call the [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) function to clear the error flag before it can begin additional I/O operations.</span></span> <span data-ttu-id="9f56c-112">**ClearCommError** informa del error específico que se ha producido y del estado actual del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f56c-112">**ClearCommError** reports the specific error that occurred and the current status of the device.</span></span>

 

 



