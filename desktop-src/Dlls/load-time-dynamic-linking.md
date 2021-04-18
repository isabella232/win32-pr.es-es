---
description: Cuando el sistema inicia un programa que usa la vinculación dinámica en tiempo de carga, usa la información del enlazador colocada en el archivo para buscar los nombres de los archivos dll utilizados por el proceso.
ms.assetid: 29a17116-bb08-4fdd-857c-b7a7f8d2278c
title: Vinculación dinámica Load-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28435fd6df4a3fc5311dc46dbb761b48c139a6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546710"
---
# <a name="load-time-dynamic-linking"></a><span data-ttu-id="c4af3-103">Vinculación dinámica Load-Time</span><span class="sxs-lookup"><span data-stu-id="c4af3-103">Load-Time Dynamic Linking</span></span>

<span data-ttu-id="c4af3-104">Cuando el sistema inicia un programa que usa la vinculación dinámica en tiempo de carga, usa la información del enlazador colocada en el archivo para buscar los nombres de los archivos dll utilizados por el proceso.</span><span class="sxs-lookup"><span data-stu-id="c4af3-104">When the system starts a program that uses load-time dynamic linking, it uses the information the linker placed in the file to locate the names of the DLLs that are used by the process.</span></span> <span data-ttu-id="c4af3-105">Después, el sistema busca los archivos dll.</span><span class="sxs-lookup"><span data-stu-id="c4af3-105">The system then searches for the DLLs.</span></span> <span data-ttu-id="c4af3-106">Para obtener más información, vea [orden de búsqueda en la biblioteca de vínculos dinámicos](dynamic-link-library-search-order.md).</span><span class="sxs-lookup"><span data-stu-id="c4af3-106">For more information, see [Dynamic-Link Library Search Order](dynamic-link-library-search-order.md).</span></span>

<span data-ttu-id="c4af3-107">Si el sistema no encuentra un archivo DLL necesario, finaliza el proceso y muestra un cuadro de diálogo que informa del error al usuario.</span><span class="sxs-lookup"><span data-stu-id="c4af3-107">If the system cannot locate a required DLL, it terminates the process and displays a dialog box that reports the error to the user.</span></span> <span data-ttu-id="c4af3-108">De lo contrario, el sistema asigna el archivo DLL en el espacio de direcciones virtuales del proceso e incrementa el recuento de referencias de DLL.</span><span class="sxs-lookup"><span data-stu-id="c4af3-108">Otherwise, the system maps the DLL into the virtual address space of the process and increments the DLL reference count.</span></span>

<span data-ttu-id="c4af3-109">El sistema llama a la función de punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="c4af3-109">The system calls the entry-point function.</span></span> <span data-ttu-id="c4af3-110">La función recibe un código que indica que el proceso está cargando el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="c4af3-110">The function receives a code indicating that the process is loading the DLL.</span></span> <span data-ttu-id="c4af3-111">Si la función de punto de entrada no devuelve el valor TRUE, el sistema finalizará el proceso y notificará un error.</span><span class="sxs-lookup"><span data-stu-id="c4af3-111">If the entry-point function does not return TRUE, the system terminates the process and reports the error.</span></span> <span data-ttu-id="c4af3-112">Para obtener más información sobre la función de punto de entrada, vea [biblioteca de vínculos dinámicos Entry-Point función](dynamic-link-library-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="c4af3-112">For more information about the entry-point function, see [Dynamic-Link Library Entry-Point Function](dynamic-link-library-entry-point-function.md).</span></span>

<span data-ttu-id="c4af3-113">Por último, el sistema modifica la tabla de direcciones de función con las direcciones de inicio de las funciones DLL importadas.</span><span class="sxs-lookup"><span data-stu-id="c4af3-113">Finally, the system modifies the function address table with the starting addresses for the imported DLL functions.</span></span>

<span data-ttu-id="c4af3-114">El archivo DLL se asigna en el espacio de direcciones virtuales del proceso durante su inicialización y se carga en la memoria física solo cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="c4af3-114">The DLL is mapped into the virtual address space of the process during its initialization and is loaded into physical memory only when needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4af3-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c4af3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4af3-116">Usar Load-Time vinculación dinámica</span><span class="sxs-lookup"><span data-stu-id="c4af3-116">Using Load-Time Dynamic Linking</span></span>](using-load-time-dynamic-linking.md)
</dt> </dl>

 

 



