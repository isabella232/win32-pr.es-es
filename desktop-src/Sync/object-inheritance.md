---
description: Cuando se crea un proceso con la función CreateProcess, se puede especificar que el proceso herede los identificadores de los objetos mutex, Event, Semaphore o Timer mediante la estructura de atributos de seguridad \_ .
ms.assetid: 36491a5c-7599-4f69-ab76-d3a62261a151
title: Herencia de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6087ae3699e7628ab97871ede41cc2e406e40157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667871"
---
# <a name="object-inheritance"></a><span data-ttu-id="aa06e-103">Herencia de objetos</span><span class="sxs-lookup"><span data-stu-id="aa06e-103">Object Inheritance</span></span>

<span data-ttu-id="aa06e-104">Cuando se crea un proceso con la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) , se puede especificar que el proceso herede los identificadores de los objetos mutex, Event, Semaphore o Timer mediante la estructura de [**\_ atributos de seguridad**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="aa06e-104">When you create a process with the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function, you can specify that the process inherit handles to mutex, event, semaphore, or timer objects using the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure.</span></span> <span data-ttu-id="aa06e-105">El identificador heredado por el proceso tiene el mismo acceso al objeto que el identificador original.</span><span class="sxs-lookup"><span data-stu-id="aa06e-105">The handle inherited by the process has the same access to the object as the original handle.</span></span> <span data-ttu-id="aa06e-106">El identificador heredado aparece en la tabla de identificadores del proceso creado, pero debe comunicar el valor de identificador al proceso creado.</span><span class="sxs-lookup"><span data-stu-id="aa06e-106">The inherited handle appears in the handle table of the created process, but you must communicate the handle value to the created process.</span></span> <span data-ttu-id="aa06e-107">Puede hacerlo especificando el valor como un argumento de línea de comandos cuando llame a **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="aa06e-107">You can do this by specifying the value as a command-line argument when you call **CreateProcess**.</span></span> <span data-ttu-id="aa06e-108">A continuación, el proceso creado utiliza la función [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) para recuperar la cadena de línea de comandos y convertir el argumento de identificador en un identificador utilizable.</span><span class="sxs-lookup"><span data-stu-id="aa06e-108">The created process then uses the [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) function to retrieve the command-line string and convert the handle argument into a usable handle.</span></span> <span data-ttu-id="aa06e-109">Para obtener más información, vea [Herencia](../procthread/inheritance.md).</span><span class="sxs-lookup"><span data-stu-id="aa06e-109">For more information, see [Inheritance](../procthread/inheritance.md).</span></span>

 

 
