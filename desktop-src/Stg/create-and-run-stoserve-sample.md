---
title: Crear y ejecutar el ejemplo StoServe
description: El ejemplo de cliente y otros ejemplos relacionados deben compilarse antes de poder ejecutar el cliente.
ms.assetid: 7d8fe758-0008-495d-89ae-a814cb07ea19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46645351eb75ceb6b4f6129049b9e8f2db59dbef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665633"
---
# <a name="create-and-run-stoserve-sample"></a><span data-ttu-id="4b2c2-103">Crear y ejecutar el ejemplo StoServe</span><span class="sxs-lookup"><span data-stu-id="4b2c2-103">Create and Run StoServe Sample</span></span>

<span data-ttu-id="4b2c2-104">El ejemplo de cliente y otros ejemplos relacionados deben compilarse antes de poder ejecutar el cliente.</span><span class="sxs-lookup"><span data-stu-id="4b2c2-104">The client sample and other related samples must be compiled before you can run the client.</span></span> <span data-ttu-id="4b2c2-105">Para obtener más información sobre la creación de los ejemplos, vea [Cómo crear ejemplos](how-to-build-samples.md).</span><span class="sxs-lookup"><span data-stu-id="4b2c2-105">For more details on building the samples, see [How to Build Samples](how-to-build-samples.md).</span></span> <span data-ttu-id="4b2c2-106">Si ya ha creado los ejemplos adecuados, STOCLIEN.EXE es el ejecutable de cliente que se ejecutará para el ejemplo **StoServe** .</span><span class="sxs-lookup"><span data-stu-id="4b2c2-106">If you have already built the appropriate samples, STOCLIEN.EXE is the client executable to run for the **StoServe** sample.</span></span>

## <a name="code-tour"></a><span data-ttu-id="4b2c2-107">Paseo por código</span><span class="sxs-lookup"><span data-stu-id="4b2c2-107">Code Tour</span></span>

<span data-ttu-id="4b2c2-108">En la tabla siguiente se enumeran los archivos pertinentes para el ejemplo **StoServe** .</span><span class="sxs-lookup"><span data-stu-id="4b2c2-108">The following table lists the files pertinent to the **StoServe** sample.</span></span>



| <span data-ttu-id="4b2c2-109">Archivos</span><span class="sxs-lookup"><span data-stu-id="4b2c2-109">Files</span></span>        | <span data-ttu-id="4b2c2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b2c2-110">Description</span></span>                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b2c2-111">STOSERVE.TXT</span><span class="sxs-lookup"><span data-stu-id="4b2c2-111">STOSERVE.TXT</span></span> | <span data-ttu-id="4b2c2-112">Breve descripción del ejemplo</span><span class="sxs-lookup"><span data-stu-id="4b2c2-112">Short sample description</span></span>                                                                                                  |
| <span data-ttu-id="4b2c2-113">MAKE</span><span class="sxs-lookup"><span data-stu-id="4b2c2-113">MAKEFILE</span></span>     | <span data-ttu-id="4b2c2-114">El archivo make genérico para generar el STOSERVE.DLL ejemplo de código de esta lección.</span><span class="sxs-lookup"><span data-stu-id="4b2c2-114">The generic makefile for building the STOSERVE.DLL code sample of this lesson.</span></span>                                            |
| <span data-ttu-id="4b2c2-115">STOSERVE. C</span><span class="sxs-lookup"><span data-stu-id="4b2c2-115">STOSERVE.H</span></span>   | <span data-ttu-id="4b2c2-116">Archivo de inclusión para declarar como importado o que define como exportado las funciones de servicio en STOSERVE.DLL.</span><span class="sxs-lookup"><span data-stu-id="4b2c2-116">The include file for declaring as imported or defining as exported the service functions in STOSERVE.DLL.</span></span>                 |
| <span data-ttu-id="4b2c2-117">STOSERVE. CPP</span><span class="sxs-lookup"><span data-stu-id="4b2c2-117">STOSERVE.CPP</span></span> | <span data-ttu-id="4b2c2-118">El archivo de implementación principal para STOSERVE.DLL.</span><span class="sxs-lookup"><span data-stu-id="4b2c2-118">The main implementation file for STOSERVE.DLL.</span></span> <span data-ttu-id="4b2c2-119">Tiene DllMain y las funciones de servidor COM (por ejemplo, DllGetClassObject).</span><span class="sxs-lookup"><span data-stu-id="4b2c2-119">Has DllMain and the COM server functions (for example, DllGetClassObject).</span></span> |
| <span data-ttu-id="4b2c2-120">STOSERVE. DEF</span><span class="sxs-lookup"><span data-stu-id="4b2c2-120">STOSERVE.DEF</span></span> | <span data-ttu-id="4b2c2-121">Archivo de definición de módulo.</span><span class="sxs-lookup"><span data-stu-id="4b2c2-121">The module definition file.</span></span> <span data-ttu-id="4b2c2-122">Exporta las funciones de alojamiento de servidor.</span><span class="sxs-lookup"><span data-stu-id="4b2c2-122">Exports server housing functions.</span></span>                                                             |
| <span data-ttu-id="4b2c2-123">STOSERVE. CR</span><span class="sxs-lookup"><span data-stu-id="4b2c2-123">STOSERVE.RC</span></span>  | <span data-ttu-id="4b2c2-124">El archivo de definición de recursos DLL para el ejecutable.</span><span class="sxs-lookup"><span data-stu-id="4b2c2-124">The DLL resource definition file for the executable.</span></span>                                                                      |
| <span data-ttu-id="4b2c2-125">STOSERVE. ICO</span><span class="sxs-lookup"><span data-stu-id="4b2c2-125">STOSERVE.ICO</span></span> | <span data-ttu-id="4b2c2-126">El recurso de icono para el ejecutable.</span><span class="sxs-lookup"><span data-stu-id="4b2c2-126">The icon resource for the executable.</span></span>                                                                                     |
| <span data-ttu-id="4b2c2-127">Servidor. C</span><span class="sxs-lookup"><span data-stu-id="4b2c2-127">SERVER.H</span></span>     | <span data-ttu-id="4b2c2-128">Archivo de inclusión para el objeto de C++ de control de servidor.</span><span class="sxs-lookup"><span data-stu-id="4b2c2-128">The include file for the server control C++ object.</span></span>                                                                       |
| <span data-ttu-id="4b2c2-129">Servidor. CPP</span><span class="sxs-lookup"><span data-stu-id="4b2c2-129">SERVER.CPP</span></span>   | <span data-ttu-id="4b2c2-130">El archivo de implementación para el objeto de C++ de control de servidor.</span><span class="sxs-lookup"><span data-stu-id="4b2c2-130">The implementation file for the server control C++ object.</span></span>                                                                |
| <span data-ttu-id="4b2c2-131">Factory. C</span><span class="sxs-lookup"><span data-stu-id="4b2c2-131">FACTORY.H</span></span>    | <span data-ttu-id="4b2c2-132">Archivo de inclusión de los objetos COM del generador de clases del servidor.</span><span class="sxs-lookup"><span data-stu-id="4b2c2-132">The include file for the server's class factory COM objects.</span></span>                                                              |
| <span data-ttu-id="4b2c2-133">Factory. CPP</span><span class="sxs-lookup"><span data-stu-id="4b2c2-133">FACTORY.CPP</span></span>  | <span data-ttu-id="4b2c2-134">El archivo de implementación para los generadores de clases del servidor.</span><span class="sxs-lookup"><span data-stu-id="4b2c2-134">The implementation file for the server's class factories.</span></span>                                                                 |
| <span data-ttu-id="4b2c2-135">Conéctelo. C</span><span class="sxs-lookup"><span data-stu-id="4b2c2-135">CONNECT.H</span></span>    | <span data-ttu-id="4b2c2-136">Archivo de inclusión para las clases de enumerador de punto de conexión, punto de conexión y enumerador de conexión.</span><span class="sxs-lookup"><span data-stu-id="4b2c2-136">The include file for the connection point enumerator, connection point, and connection enumerator classes.</span></span>                |
| <span data-ttu-id="4b2c2-137">Conéctelo. CPP</span><span class="sxs-lookup"><span data-stu-id="4b2c2-137">CONNECT.CPP</span></span>  | <span data-ttu-id="4b2c2-138">El archivo de implementación para el enumerador de puntos de conexión, el punto de conexión y los objetos de enumerador de conexión.</span><span class="sxs-lookup"><span data-stu-id="4b2c2-138">The implementation file for the connection point enumerator, connection point, and connection enumerator objects.</span></span>         |
| <span data-ttu-id="4b2c2-139">Papel. C</span><span class="sxs-lookup"><span data-stu-id="4b2c2-139">PAPER.H</span></span>      | <span data-ttu-id="4b2c2-140">Archivo de inclusión de la clase de objeto COM de copaper.</span><span class="sxs-lookup"><span data-stu-id="4b2c2-140">The include file for the COPaper COM object class.</span></span>                                                                        |
| <span data-ttu-id="4b2c2-141">Papel. CPP</span><span class="sxs-lookup"><span data-stu-id="4b2c2-141">PAPER.CPP</span></span>    | <span data-ttu-id="4b2c2-142">El archivo de implementación para la clase de objeto COM de copaper y los puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="4b2c2-142">The implementation file for the COPaper COM object class and the connection points.</span></span>                                       |
| <span data-ttu-id="4b2c2-143">STOSERVE. DSP</span><span class="sxs-lookup"><span data-stu-id="4b2c2-143">STOSERVE.DSP</span></span> | <span data-ttu-id="4b2c2-144">Microsoft Visual Studio archivo de proyecto.</span><span class="sxs-lookup"><span data-stu-id="4b2c2-144">Microsoft Visual Studio Project file.</span></span>                                                                                     |



 

<span data-ttu-id="4b2c2-145">Los temas principales que se tratan en este tutorial de código son:</span><span class="sxs-lookup"><span data-stu-id="4b2c2-145">The major topics covered in this code tour are:</span></span>

-   <span data-ttu-id="4b2c2-146">Los métodos de la interfaz [**IPaper**](ipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="4b2c2-146">The [**IPaper**](ipaper-methods.md) interface methods.</span></span>
-   <span data-ttu-id="4b2c2-147">El uso del copaper de la interfaz [**IPaperSink**](ipapersink-methods.md) para las notificaciones de cliente.</span><span class="sxs-lookup"><span data-stu-id="4b2c2-147">COPaper's use of the [**IPaperSink**](ipapersink-methods.md) interface for client notifications.</span></span>
-   <span data-ttu-id="4b2c2-148">[**Estructuras**](structures---stoserve.md) en StoServe.</span><span class="sxs-lookup"><span data-stu-id="4b2c2-148">[**Structures**](structures---stoserve.md) in StoServe.</span></span>
-   <span data-ttu-id="4b2c2-149">[Consideraciones de Unicode](unicode-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="4b2c2-149">[Unicode considerations](unicode-considerations.md).</span></span>

 

 




