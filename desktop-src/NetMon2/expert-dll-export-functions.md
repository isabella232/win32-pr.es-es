---
description: Las siguientes funciones son los puntos de entrada de los archivos dll expertos y las llamadas del sistema operativo y Monitor de red.
ms.assetid: 1c0dcf6f-7f80-424b-9e6a-5a8b6a5b176f
title: Funciones de exportación de archivos DLL de experto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923611521b98619b357eb2de93ee2269caf9c838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000944"
---
# <a name="expert-dll-export-functions"></a><span data-ttu-id="64866-103">Funciones de exportación de archivos DLL de experto</span><span class="sxs-lookup"><span data-stu-id="64866-103">Expert DLL Export Functions</span></span>

<span data-ttu-id="64866-104">Las siguientes funciones son los puntos de entrada de los archivos dll expertos y las llamadas del sistema operativo y Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="64866-104">The following functions are the entry points for expert DLLs and for calls from the operating system and Network Monitor.</span></span>



| <span data-ttu-id="64866-105">Función</span><span class="sxs-lookup"><span data-stu-id="64866-105">Function</span></span>                                   | <span data-ttu-id="64866-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="64866-106">Description</span></span>                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64866-107">**Experto de DllMain**</span><span class="sxs-lookup"><span data-stu-id="64866-107">**DllMain Expert**</span></span>](dllmain-expert.md)   | <span data-ttu-id="64866-108">Indica que se ha cargado o descargado el archivo DLL de expertos.</span><span class="sxs-lookup"><span data-stu-id="64866-108">Indicates that the expert DLL has been loaded or unloaded.</span></span> <span data-ttu-id="64866-109">Cuando un proceso carga o descarga el archivo DLL, el sistema operativo llama a la función [**DllMain**](/windows/desktop/Dlls/dllmain) .</span><span class="sxs-lookup"><span data-stu-id="64866-109">When a process loads or unloads the DLL, the operating system calls the [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span> |
| [<span data-ttu-id="64866-110">**Registrar experto**</span><span class="sxs-lookup"><span data-stu-id="64866-110">**Register Expert**</span></span>](register-expert.md) | <span data-ttu-id="64866-111">Determina la información básica sobre el experto en el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="64866-111">Determines basic information about the expert within the DLL.</span></span> <span data-ttu-id="64866-112">Monitor de red llama a la función **Register** .</span><span class="sxs-lookup"><span data-stu-id="64866-112">Network Monitor calls the **Register** function.</span></span>                                                           |
| [<span data-ttu-id="64866-113">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="64866-113">**Configure**</span></span>](configure.md)             | <span data-ttu-id="64866-114">Configura el experto en el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="64866-114">Configures the expert within the DLL.</span></span> <span data-ttu-id="64866-115">Monitor de red llama a la función de [**configuración**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="64866-115">Network Monitor calls the [**Configure**](configure.md) function.</span></span>                                                                 |
| [<span data-ttu-id="64866-116">**Ejecutar**</span><span class="sxs-lookup"><span data-stu-id="64866-116">**Run**</span></span>](run.md)                         | <span data-ttu-id="64866-117">Inicia el experto en el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="64866-117">Starts the expert within the DLL.</span></span> <span data-ttu-id="64866-118">Monitor de red llama a la función de [**ejecución**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="64866-118">Network Monitor calls the [**Run**](run.md) function.</span></span>                                                                                 |



 

<span data-ttu-id="64866-119">Monitor de red también proporciona estructuras, enumeraciones y funciones auxiliares a las que puede llamar el experto.</span><span class="sxs-lookup"><span data-stu-id="64866-119">Network Monitor also provides structures, enumerations, and helper functions that the expert can call.</span></span>



| <span data-ttu-id="64866-120">Para información acerca de</span><span class="sxs-lookup"><span data-stu-id="64866-120">For information about</span></span>                                      | <span data-ttu-id="64866-121">Vea</span><span class="sxs-lookup"><span data-stu-id="64866-121">See</span></span>                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="64866-122">Funciones auxiliares a las que pueden llamar expertos y analizadores</span><span class="sxs-lookup"><span data-stu-id="64866-122">Helper functions that can be called by experts and parsers</span></span> | [<span data-ttu-id="64866-123">Funciones comunes de experto y analizador</span><span class="sxs-lookup"><span data-stu-id="64866-123">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |
| <span data-ttu-id="64866-124">Funciones auxiliares a las que solo llaman expertos</span><span class="sxs-lookup"><span data-stu-id="64866-124">Helper functions that are called only by experts</span></span>           | [<span data-ttu-id="64866-125">Funciones de experto</span><span class="sxs-lookup"><span data-stu-id="64866-125">Expert Functions</span></span>](expert-functions.md)                                     |
| <span data-ttu-id="64866-126">Estructuras usadas por las funciones de expertos</span><span class="sxs-lookup"><span data-stu-id="64866-126">Structures that are used by expert functions</span></span>               | [<span data-ttu-id="64866-127">Estructuras expertas</span><span class="sxs-lookup"><span data-stu-id="64866-127">Expert Structures</span></span>](expert-structures.md)                                   |
| <span data-ttu-id="64866-128">Enumeraciones usadas por las estructuras y funciones de expertos</span><span class="sxs-lookup"><span data-stu-id="64866-128">Enumerations used by expert structures and functions</span></span>       | [<span data-ttu-id="64866-129">Enumeraciones de experto</span><span class="sxs-lookup"><span data-stu-id="64866-129">Expert Enumerations</span></span>](expert-enumerations.md)                               |



 

 

 
