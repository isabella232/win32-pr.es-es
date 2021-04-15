---
description: Un proceso secundario puede heredar los identificadores de su proceso primario. Un identificador heredado solo es válido en el contexto del proceso secundario. Para permitir que un proceso secundario herede los identificadores abiertos de su proceso primario, siga estos pasos.
ms.assetid: 957cd369-bebf-4e04-9f7e-a936e2e97887
title: Controlar la herencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd684308503a8747f6730e9d0daf4aa3de760186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668448"
---
# <a name="handle-inheritance"></a><span data-ttu-id="1f16c-105">Controlar la herencia</span><span class="sxs-lookup"><span data-stu-id="1f16c-105">Handle Inheritance</span></span>

<span data-ttu-id="1f16c-106">Un proceso secundario puede heredar los identificadores de su proceso primario.</span><span class="sxs-lookup"><span data-stu-id="1f16c-106">A child process can inherit handles from its parent process.</span></span> <span data-ttu-id="1f16c-107">Un identificador heredado solo es válido en el contexto del proceso secundario.</span><span class="sxs-lookup"><span data-stu-id="1f16c-107">An inherited handle is valid only in the context of the child process.</span></span> <span data-ttu-id="1f16c-108">Para permitir que un proceso secundario herede los identificadores abiertos de su proceso primario, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="1f16c-108">To enable a child process to inherit open handles from its parent process, use the following steps.</span></span>

1.  <span data-ttu-id="1f16c-109">Cree el identificador con el miembro **bInheritHandle** de la estructura de [**\_ atributos de seguridad**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="1f16c-109">Create the handle with the **bInheritHandle** member of the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure set to **TRUE**.</span></span>
2.  <span data-ttu-id="1f16c-110">Cree el proceso secundario con la función [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) , con el parámetro *BInheritHandles* establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="1f16c-110">Create the child process using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function, with the *bInheritHandles* parameter set to **TRUE**.</span></span>

<span data-ttu-id="1f16c-111">La función [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) duplica un identificador que se va a usar en el proceso actual o en otro proceso.</span><span class="sxs-lookup"><span data-stu-id="1f16c-111">The [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function duplicates a handle to be used in the current process or in another process.</span></span> <span data-ttu-id="1f16c-112">Si una aplicación duplica uno de sus identificadores para otro proceso, el identificador duplicado solo es válido en el contexto del otro proceso.</span><span class="sxs-lookup"><span data-stu-id="1f16c-112">If an application duplicates one of its handles for another process, the duplicated handle is valid only in the context of the other process.</span></span>

<span data-ttu-id="1f16c-113">Un identificador duplicado o heredado es un valor único, pero hace referencia al mismo objeto que el identificador original.</span><span class="sxs-lookup"><span data-stu-id="1f16c-113">A duplicated or inherited handle is a unique value, but it refers to the same object as the original handle.</span></span> <span data-ttu-id="1f16c-114">Los procesos pueden heredar o duplicar los identificadores de los siguientes tipos de objetos:</span><span class="sxs-lookup"><span data-stu-id="1f16c-114">Processes can inherit or duplicate handles to the following types of objects:</span></span>

-   <span data-ttu-id="1f16c-115">Token de acceso</span><span class="sxs-lookup"><span data-stu-id="1f16c-115">Access Token</span></span>
-   <span data-ttu-id="1f16c-116">Dispositivo de comunicaciones</span><span class="sxs-lookup"><span data-stu-id="1f16c-116">Communications device</span></span>
-   <span data-ttu-id="1f16c-117">Entrada de la consola</span><span class="sxs-lookup"><span data-stu-id="1f16c-117">Console input</span></span>
-   <span data-ttu-id="1f16c-118">Búfer de pantalla de la consola</span><span class="sxs-lookup"><span data-stu-id="1f16c-118">Console screen buffer</span></span>
-   <span data-ttu-id="1f16c-119">Escritorio</span><span class="sxs-lookup"><span data-stu-id="1f16c-119">Desktop</span></span>
-   <span data-ttu-id="1f16c-120">Directorio</span><span class="sxs-lookup"><span data-stu-id="1f16c-120">Directory</span></span>
-   <span data-ttu-id="1f16c-121">Evento</span><span class="sxs-lookup"><span data-stu-id="1f16c-121">Event</span></span>
-   <span data-ttu-id="1f16c-122">Archivo</span><span class="sxs-lookup"><span data-stu-id="1f16c-122">File</span></span>
-   <span data-ttu-id="1f16c-123">Asignación de archivos</span><span class="sxs-lookup"><span data-stu-id="1f16c-123">File mapping</span></span>
-   <span data-ttu-id="1f16c-124">Trabajo</span><span class="sxs-lookup"><span data-stu-id="1f16c-124">Job</span></span>
-   <span data-ttu-id="1f16c-125">Datagrama</span><span class="sxs-lookup"><span data-stu-id="1f16c-125">Mailslot</span></span>
-   <span data-ttu-id="1f16c-126">Mutex</span><span class="sxs-lookup"><span data-stu-id="1f16c-126">Mutex</span></span>
-   <span data-ttu-id="1f16c-127">Pipe</span><span class="sxs-lookup"><span data-stu-id="1f16c-127">Pipe</span></span>
-   <span data-ttu-id="1f16c-128">Proceso</span><span class="sxs-lookup"><span data-stu-id="1f16c-128">Process</span></span>
-   <span data-ttu-id="1f16c-129">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="1f16c-129">Registry key</span></span>
-   <span data-ttu-id="1f16c-130">Semaphore</span><span class="sxs-lookup"><span data-stu-id="1f16c-130">Semaphore</span></span>
-   <span data-ttu-id="1f16c-131">Toma de corriente</span><span class="sxs-lookup"><span data-stu-id="1f16c-131">Socket</span></span>
-   <span data-ttu-id="1f16c-132">Thread</span><span class="sxs-lookup"><span data-stu-id="1f16c-132">Thread</span></span>
-   <span data-ttu-id="1f16c-133">Temporizador</span><span class="sxs-lookup"><span data-stu-id="1f16c-133">Timer</span></span>
-   <span data-ttu-id="1f16c-134">Estación de ventana</span><span class="sxs-lookup"><span data-stu-id="1f16c-134">Window station</span></span>

<span data-ttu-id="1f16c-135">Todos los demás objetos son privados para el proceso que los creó. los identificadores de objeto no se pueden duplicar ni heredar.</span><span class="sxs-lookup"><span data-stu-id="1f16c-135">All other objects are private to the process that created them; their object handles cannot be duplicated or inherited.</span></span>

<span data-ttu-id="1f16c-136">Para obtener más información, vea [Herencia](/windows/desktop/ProcThread/inheritance).</span><span class="sxs-lookup"><span data-stu-id="1f16c-136">For more information, see [Inheritance](/windows/desktop/ProcThread/inheritance).</span></span>

 

 
