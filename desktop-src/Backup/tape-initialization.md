---
title: Inicialización de cinta
description: Una aplicación debe utilizar la función CreateFile para crear un identificador de un dispositivo de cinta. Este identificador se usa en operaciones posteriores en la cinta del dispositivo.
ms.assetid: 5e7eddd2-8137-4e79-b1ee-c371bc4c7f75
keywords:
- Copia de seguridad de inicialización de cinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64f77b5c4d52641d2a3f195d517e575c9e2f780f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488002"
---
# <a name="tape-initialization"></a><span data-ttu-id="7584e-105">Inicialización de cinta</span><span class="sxs-lookup"><span data-stu-id="7584e-105">Tape Initialization</span></span>

<span data-ttu-id="7584e-106">Una aplicación debe utilizar la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para crear un identificador de un dispositivo de cinta.</span><span class="sxs-lookup"><span data-stu-id="7584e-106">An application must use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to create a handle of a tape device.</span></span> <span data-ttu-id="7584e-107">Este identificador se usa en operaciones posteriores en la cinta del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7584e-107">This handle is used in subsequent operations on the tape in the device.</span></span>

<span data-ttu-id="7584e-108">Antes de que una aplicación escriba en una cinta, la cinta debe estar formateada según las necesidades de la aplicación y las capacidades de la unidad de cinta que se está usando.</span><span class="sxs-lookup"><span data-stu-id="7584e-108">Before an application writes to a tape, the tape must be formatted according to the needs of the application and the capabilities of the tape drive being used.</span></span> <span data-ttu-id="7584e-109">La función [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) cambia el formato de una cinta y crea en ella un número determinado de particiones de un tamaño especificado.</span><span class="sxs-lookup"><span data-stu-id="7584e-109">The [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) function reformats a tape, creating on it a given number of partitions of a specified size.</span></span>

<span data-ttu-id="7584e-110">La función [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape) prepara una cinta para tener acceso a ella o quitarla.</span><span class="sxs-lookup"><span data-stu-id="7584e-110">The [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape) function prepares a tape to be accessed or removed.</span></span> <span data-ttu-id="7584e-111">Esta función puede cargar, descargar, bloquear o desbloquear una cinta.</span><span class="sxs-lookup"><span data-stu-id="7584e-111">This function can load, unload, lock, or unlock a tape.</span></span> <span data-ttu-id="7584e-112">Esta función también puede tensar la cinta moviendo la cinta hasta el final de la cinta y volviendo al principio.</span><span class="sxs-lookup"><span data-stu-id="7584e-112">This function can also tension the tape by moving the tape to the end of the tape and back to the beginning.</span></span>

<span data-ttu-id="7584e-113">Para recuperar y establecer información sobre una cinta y una unidad de cinta, una aplicación usa las funciones [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters), [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)y [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) .</span><span class="sxs-lookup"><span data-stu-id="7584e-113">To retrieve and set information about a tape and tape drive, an application uses the [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters), [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters), and [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) functions.</span></span>

<span data-ttu-id="7584e-114">[**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) recupera información que describe una cinta o una unidad de cinta.</span><span class="sxs-lookup"><span data-stu-id="7584e-114">[**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) retrieves information that describes a tape or a tape drive.</span></span> <span data-ttu-id="7584e-115">La información de la cinta incluye el tipo de cinta, la densidad y el tamaño de bloque; el número de particiones de la cinta; la cantidad de cinta restante; etc.</span><span class="sxs-lookup"><span data-stu-id="7584e-115">The tape information includes the tape's type, density, and block size; the number of partitions on the tape; the amount of tape remaining; and so on.</span></span> <span data-ttu-id="7584e-116">La información de la unidad de cinta incluye el tamaño de bloque predeterminado de la unidad, el número máximo de particiones y las características que se admiten.</span><span class="sxs-lookup"><span data-stu-id="7584e-116">The tape drive information includes the drive's default block size, the maximum partition count, and the features that are supported.</span></span>

<span data-ttu-id="7584e-117">[**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) establece el tamaño del bloque de cinta o establece las marcas de la unidad de cinta que indican si la unidad admite la corrección de errores de hardware, la compresión de datos, el relleno de datos o cualquier combinación de los tres.</span><span class="sxs-lookup"><span data-stu-id="7584e-117">[**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) either sets the tape block size or sets the tape drive flags that indicate whether the drive supports hardware error correction, data compression, data padding, or any combination of the three.</span></span>

<span data-ttu-id="7584e-118">[**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) indica si la unidad de cinta está lista para procesar comandos de cinta.</span><span class="sxs-lookup"><span data-stu-id="7584e-118">[**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) indicates whether the tape drive is ready to process tape commands.</span></span>

 

 