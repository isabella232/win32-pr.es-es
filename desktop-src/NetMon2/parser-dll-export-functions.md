---
description: Las funciones, enumeradas en la tabla siguiente, son puntos de entrada para los archivos DLL del analizador. Las funciones son los puntos de entrada para las llamadas desde el sistema operativo y Monitor de red.
ms.assetid: 67811ddb-1961-4306-a62f-b9fd2d2d2b55
title: Funciones de exportación de DLL de analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929541a1eda60740fe219352fee285a5a34a89df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423675"
---
# <a name="parser-dll-export-functions"></a><span data-ttu-id="37a6a-104">Funciones de exportación de DLL de analizador</span><span class="sxs-lookup"><span data-stu-id="37a6a-104">Parser DLL Export Functions</span></span>

<span data-ttu-id="37a6a-105">Las funciones, enumeradas en la tabla siguiente, son puntos de entrada para los archivos DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="37a6a-105">The functions, listed in the following table, are entry points for parser DLLs.</span></span> <span data-ttu-id="37a6a-106">Las funciones son los puntos de entrada para las llamadas desde el sistema operativo y Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="37a6a-106">The functions are the entry points for calls from the operating system and Network Monitor.</span></span>



| <span data-ttu-id="37a6a-107">Función</span><span class="sxs-lookup"><span data-stu-id="37a6a-107">Function</span></span>                                           | <span data-ttu-id="37a6a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="37a6a-108">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37a6a-109">Analizador de DllMain</span><span class="sxs-lookup"><span data-stu-id="37a6a-109">DllMain Parser</span></span>](dllmain-parser.md)               | <span data-ttu-id="37a6a-110">Indica al archivo DLL del analizador que está cargado o descargado.</span><span class="sxs-lookup"><span data-stu-id="37a6a-110">Indicates to the parser DLL that it is loaded or unloaded.</span></span> <span data-ttu-id="37a6a-111">El sistema operativo llama a la función de **analizador DllMain** cuando un proceso carga o descarga el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="37a6a-111">The operating system calls the **DllMain Parser** function when a process loads or unloads the DLL.</span></span> |
| [<span data-ttu-id="37a6a-112">AttachProperties</span><span class="sxs-lookup"><span data-stu-id="37a6a-112">AttachProperties</span></span>](attachproperties.md)           | <span data-ttu-id="37a6a-113">Notifica al analizador que debe adjuntar cualquier propiedad que exista en un marco.</span><span class="sxs-lookup"><span data-stu-id="37a6a-113">Notifies the parser to attach any properties that exist in a frame.</span></span>                                                                                            |
| [<span data-ttu-id="37a6a-114">Eliminar registro</span><span class="sxs-lookup"><span data-stu-id="37a6a-114">Deregister</span></span>](deregister.md)                       | <span data-ttu-id="37a6a-115">Notifica al analizador que se va a limpiar.</span><span class="sxs-lookup"><span data-stu-id="37a6a-115">Notifies the parser to clean up.</span></span>                                                                                                                               |
| [<span data-ttu-id="37a6a-116">FormatProperties</span><span class="sxs-lookup"><span data-stu-id="37a6a-116">FormatProperties</span></span>](formatproperties.md)           | <span data-ttu-id="37a6a-117">Notifica al analizador que debe tomar todas las instancias de propiedad de y compilar el miembro **szPropertyText** de cada estructura **PROPERTYINST** .</span><span class="sxs-lookup"><span data-stu-id="37a6a-117">Notifies the parser to take all of the property instances in and build the **szPropertyText** member of each **PROPERTYINST** structure.</span></span>                       |
| [<span data-ttu-id="37a6a-118">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="37a6a-118">RecognizeFrame</span></span>](recognizeframe.md)               | <span data-ttu-id="37a6a-119">Determina si el analizador puede interpretar los datos del marco sin procesar con el protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="37a6a-119">Determines whether the parser can interpret the unprocessed frame data with the specified protocol.</span></span>                                                            |
| [<span data-ttu-id="37a6a-120">Registrar analizador</span><span class="sxs-lookup"><span data-stu-id="37a6a-120">Register Parser</span></span>](register-parser.md)             | <span data-ttu-id="37a6a-121">Determina la información básica sobre el analizador en el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="37a6a-121">Determines basic information about the parser within the DLL.</span></span> <span data-ttu-id="37a6a-122">Monitor de red llama a la función **Register parser** .</span><span class="sxs-lookup"><span data-stu-id="37a6a-122">Network Monitor calls the **Register Parser** function.</span></span>                                          |
| [<span data-ttu-id="37a6a-123">ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="37a6a-123">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md) | <span data-ttu-id="37a6a-124">Instala un analizador automáticamente.</span><span class="sxs-lookup"><span data-stu-id="37a6a-124">Installs a parser automatically.</span></span>                                                                                                                               |



 

<span data-ttu-id="37a6a-125">Monitor de red proporciona las estructuras y las funciones auxiliares a las que puede llamar el analizador.</span><span class="sxs-lookup"><span data-stu-id="37a6a-125">Network Monitor provides structures and helper functions that the parser can call.</span></span>



| <span data-ttu-id="37a6a-126">Para más información sobre</span><span class="sxs-lookup"><span data-stu-id="37a6a-126">For more information about</span></span>                          | <span data-ttu-id="37a6a-127">Vea</span><span class="sxs-lookup"><span data-stu-id="37a6a-127">See</span></span>                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="37a6a-128">Funciones auxiliares a las que pueden llamar los expertos y analizadores.</span><span class="sxs-lookup"><span data-stu-id="37a6a-128">Helper functions that experts and parsers can call.</span></span> | [<span data-ttu-id="37a6a-129">Funciones comunes de experto y analizador</span><span class="sxs-lookup"><span data-stu-id="37a6a-129">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |
| <span data-ttu-id="37a6a-130">Funciones auxiliares a las que solo pueden llamar los analizadores.</span><span class="sxs-lookup"><span data-stu-id="37a6a-130">Helper functions that only parsers can call.</span></span>        | [<span data-ttu-id="37a6a-131">Funciones de analizador</span><span class="sxs-lookup"><span data-stu-id="37a6a-131">Parser Functions</span></span>](parser-functions.md)                                     |
| <span data-ttu-id="37a6a-132">Estructuras que usan las funciones de analizador.</span><span class="sxs-lookup"><span data-stu-id="37a6a-132">Structures that parser functions use.</span></span>               | [<span data-ttu-id="37a6a-133">Estructuras de analizador</span><span class="sxs-lookup"><span data-stu-id="37a6a-133">Parser Structures</span></span>](parser-structures.md)                                   |



 

 

 



