---
description: Descripciones de las funciones que se van a usar al trabajar con buzones de trabajo, clientes y servidores.
ms.assetid: 40758d5e-8538-47d9-b8ca-8de5b053ee8b
title: Operaciones de buzón de correo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0055ad434971659dc2cfd058146029bb63023654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716157"
---
# <a name="mailslot-operations"></a><span data-ttu-id="738c8-103">Operaciones de buzón de correo</span><span class="sxs-lookup"><span data-stu-id="738c8-103">Mailslot Operations</span></span>

<span data-ttu-id="738c8-104">Cuando se trabaja con buzones de trabajo, los clientes y los servidores deben utilizar solo las funciones descritas en las tablas siguientes.</span><span class="sxs-lookup"><span data-stu-id="738c8-104">When working with mailslots, clients and servers should use only the functions discussed in the following tables.</span></span> <span data-ttu-id="738c8-105">No use otras funciones, aunque acepten identificadores de archivo o nombres de archivo como parámetros, ya que no están diseñados para trabajar con los buzones de archivos.</span><span class="sxs-lookup"><span data-stu-id="738c8-105">Do not use other functions, even if they accept file handles or file names as parameters, as they are not designed to work with mailslots.</span></span>

## <a name="mailslot-server-functions"></a><span data-ttu-id="738c8-106">Funciones de servidor de buzón de correo</span><span class="sxs-lookup"><span data-stu-id="738c8-106">Mailslot Server Functions</span></span>

<span data-ttu-id="738c8-107">Los servidores de buzón de correo tienen el uso exclusivo de tres funciones, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="738c8-107">Mailslot servers have exclusive use of three functions, as shown in the following table.</span></span>



| <span data-ttu-id="738c8-108">Función</span><span class="sxs-lookup"><span data-stu-id="738c8-108">Function</span></span>                                   | <span data-ttu-id="738c8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="738c8-109">Description</span></span>                                                                                                                                                                                                  |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="738c8-110">**CreateMailslot**</span><span class="sxs-lookup"><span data-stu-id="738c8-110">**CreateMailslot**</span></span>](/windows/desktop/api/Winbase/nf-winbase-createmailslota)   | <span data-ttu-id="738c8-111">Crea un buzón de correo y devuelve un identificador de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="738c8-111">Creates a mailslot and returns a mailslot handle.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="738c8-112">**GetMailslotInfo**</span><span class="sxs-lookup"><span data-stu-id="738c8-112">**GetMailslotInfo**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) | <span data-ttu-id="738c8-113">Recupera el tamaño máximo del mensaje, el tamaño del procesador de mensajes, el tamaño del siguiente mensaje en el buzón de correo, el número de mensajes del buzón de correo y la cantidad de tiempo que una operación de lectura puede esperar a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="738c8-113">Retrieves the maximum message size, the mailslot size, the size of the next message in the mailslot, the number of messages in the mailslot, and the amount of time a read operation can wait for a message.</span></span> |
| [<span data-ttu-id="738c8-114">**SetMailslotInfo**</span><span class="sxs-lookup"><span data-stu-id="738c8-114">**SetMailslotInfo**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo) | <span data-ttu-id="738c8-115">Cambia el tiempo de espera de lectura de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="738c8-115">Changes the read time-out for a mailslot.</span></span>                                                                                                                                                                    |



 

<span data-ttu-id="738c8-116">Los servidores de buzón de correo también usan las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="738c8-116">The following functions are also used by mailslot servers.</span></span>



| <span data-ttu-id="738c8-117">Función</span><span class="sxs-lookup"><span data-stu-id="738c8-117">Function</span></span>                                                         | <span data-ttu-id="738c8-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="738c8-118">Description</span></span>                                         |
|------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="738c8-119">**DuplicateHandle**</span><span class="sxs-lookup"><span data-stu-id="738c8-119">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                      | <span data-ttu-id="738c8-120">Duplica el identificador de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="738c8-120">Duplicates the mailslot handle.</span></span>                     |
| <span data-ttu-id="738c8-121">[**Readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [ **ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)</span><span class="sxs-lookup"><span data-stu-id="738c8-121">[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)</span></span> | <span data-ttu-id="738c8-122">Recupera mensajes de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="738c8-122">Retrieves messages from a mailslot.</span></span>                 |
| [<span data-ttu-id="738c8-123">**GetFileTime**</span><span class="sxs-lookup"><span data-stu-id="738c8-123">**GetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | <span data-ttu-id="738c8-124">Recupera la fecha y hora en que se creó un buzón.</span><span class="sxs-lookup"><span data-stu-id="738c8-124">Retrieves the date and time a mailslot was created.</span></span> |
| [<span data-ttu-id="738c8-125">**SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="738c8-125">**SetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | <span data-ttu-id="738c8-126">Establece la fecha y hora en que se creó un buzón.</span><span class="sxs-lookup"><span data-stu-id="738c8-126">Sets the date and time a mailslot was created.</span></span>      |
| [<span data-ttu-id="738c8-127">**GetHandleInformation**</span><span class="sxs-lookup"><span data-stu-id="738c8-127">**GetHandleInformation**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-gethandleinformation)            | <span data-ttu-id="738c8-128">Recupera las propiedades del identificador de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="738c8-128">Retrieves properties of the mailslot handle.</span></span>        |
| [<span data-ttu-id="738c8-129">**SetHandleInformation**</span><span class="sxs-lookup"><span data-stu-id="738c8-129">**SetHandleInformation**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation)            | <span data-ttu-id="738c8-130">Establece las propiedades del identificador de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="738c8-130">Sets properties of the mailslot handle.</span></span>             |



 

## <a name="mailslot-client-functions"></a><span data-ttu-id="738c8-131">Funciones de cliente de buzón de correo</span><span class="sxs-lookup"><span data-stu-id="738c8-131">Mailslot Client Functions</span></span>

<span data-ttu-id="738c8-132">Un proceso de cliente utiliza las siguientes funciones al interactuar con un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="738c8-132">A client process uses the following functions when interacting with a mailslot.</span></span>



| <span data-ttu-id="738c8-133">Función</span><span class="sxs-lookup"><span data-stu-id="738c8-133">Function</span></span>                                                             | <span data-ttu-id="738c8-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="738c8-134">Description</span></span>                                     |
|----------------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="738c8-135">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="738c8-135">**CloseHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-closehandle)                                  | <span data-ttu-id="738c8-136">Cierra un identificador de buzón de correo para un proceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="738c8-136">Closes a mailslot handle for a client process.</span></span>  |
| [<span data-ttu-id="738c8-137">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="738c8-137">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)                                    | <span data-ttu-id="738c8-138">Crea un identificador de buzón de correo para un proceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="738c8-138">Creates a mailslot handle for a client process.</span></span> |
| [<span data-ttu-id="738c8-139">**DuplicateHandle**</span><span class="sxs-lookup"><span data-stu-id="738c8-139">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                          | <span data-ttu-id="738c8-140">Duplica un identificador de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="738c8-140">Duplicates a mailslot handle.</span></span>                   |
| <span data-ttu-id="738c8-141">[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [ **WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex)</span><span class="sxs-lookup"><span data-stu-id="738c8-141">[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex)</span></span> | <span data-ttu-id="738c8-142">Escribe datos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="738c8-142">Writes data to a mailslot.</span></span>                      |



 

 

 
