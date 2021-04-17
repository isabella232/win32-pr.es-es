---
description: Es similar a un modificador de la línea de comandos. Sin embargo, no es necesario volver a escribir un \# comando pragma cada vez que se compila un archivo MOF.
ms.assetid: 3cf22686-dd56-43a3-9584-3d707a20a3a0
ms.tgt_platform: multiple
title: '#pragma'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ae13d5f960e0b415f34dce97a40cff6cba8056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697647"
---
# <a name="pragma"></a><span data-ttu-id="401c2-104">\#pragma</span><span class="sxs-lookup"><span data-stu-id="401c2-104">\#pragma</span></span>

<span data-ttu-id="401c2-105">El comando de preprocesador **\# pragma** es similar a un modificador de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="401c2-105">The **\#pragma** preprocessor command is similar to a command-line switch.</span></span> <span data-ttu-id="401c2-106">Sin embargo, no es necesario volver a escribir un comando **\# pragma** cada vez que se COMPILA un archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="401c2-106">However, you do not need to reenter a **\#pragma** command each time you compile a MOF file.</span></span> <span data-ttu-id="401c2-107">En el ejemplo siguiente se muestra la sintaxis del comando **\# pragma** :</span><span class="sxs-lookup"><span data-stu-id="401c2-107">The following example illustrates **\#pragma** command syntax:</span></span>


```mof
#pragma [command]
```



<span data-ttu-id="401c2-108">Normalmente, se coloca un comando **\# pragma** al principio de un archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="401c2-108">You usually place a **\#pragma** command at the beginning of a MOF file.</span></span> <span data-ttu-id="401c2-109">No obstante, puede colocar algunos comandos, como el comando **\# pragma** , en el cuerpo del código MOF.</span><span class="sxs-lookup"><span data-stu-id="401c2-109">However, you can place some commands, such as the **\#pragma** command, in the body of your MOF code.</span></span> <span data-ttu-id="401c2-110">En el ejemplo siguiente se muestran comandos **\# pragma** que indican al compilador MOF que debe colocar clases e instancias en el \\ espacio de nombres root cimv2 y compilar el archivo en el que se incluyen los comandos durante la recuperación del repositorio:</span><span class="sxs-lookup"><span data-stu-id="401c2-110">The following example shows **\#pragma** commands that indicate to the MOF compiler that it must place classes and instances in the root\\cimv2 namespace and compile the file in which the commands are included during repository recovery:</span></span>


```mof
#pragma autorecover
#pragma namespace ("\\\\.\\root\\cimv2")
```



<span data-ttu-id="401c2-111">A continuación se enumeran los comandos de **\# pragma** disponibles.</span><span class="sxs-lookup"><span data-stu-id="401c2-111">The following lists the available **\#pragma** commands.</span></span>



| <span data-ttu-id="401c2-112">Get-Help</span><span class="sxs-lookup"><span data-stu-id="401c2-112">Command</span></span>                                         | <span data-ttu-id="401c2-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="401c2-113">Description</span></span>                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="401c2-114">**corrección**</span><span class="sxs-lookup"><span data-stu-id="401c2-114">**amendment**</span></span>](pragma-amendment.md)           | <span data-ttu-id="401c2-115">Indica al compilador MOF que separe un archivo MOF en versiones independientes del lenguaje y específicas del idioma.</span><span class="sxs-lookup"><span data-stu-id="401c2-115">Directs the MOF compiler to separate a MOF file into language-neutral and language-specific versions.</span></span> |
| [<span data-ttu-id="401c2-116">**Autorrecuperación**</span><span class="sxs-lookup"><span data-stu-id="401c2-116">**autorecover**</span></span>](pragma-autorecover.md)       | <span data-ttu-id="401c2-117">Agrega un archivo MOF a la lista de archivos compilados durante la recuperación del repositorio.</span><span class="sxs-lookup"><span data-stu-id="401c2-117">Adds a MOF file to the list of files compiled during repository recovery.</span></span>                             |
| [<span data-ttu-id="401c2-118">**classflags**</span><span class="sxs-lookup"><span data-stu-id="401c2-118">**classflags**</span></span>](pragma-classflags.md)         | <span data-ttu-id="401c2-119">Controla la forma en que se crean o actualizan las clases según las marcas especificadas.</span><span class="sxs-lookup"><span data-stu-id="401c2-119">Controls the way classes are created or updated depending on the flags specified.</span></span>                     |
| [<span data-ttu-id="401c2-120">**deleteclass**</span><span class="sxs-lookup"><span data-stu-id="401c2-120">**deleteclass**</span></span>](pragma-deleteclass.md)       | <span data-ttu-id="401c2-121">Elimina una clase existente y sus instancias del repositorio.</span><span class="sxs-lookup"><span data-stu-id="401c2-121">Deletes an existing class and its instances from the repository.</span></span>                                      |
| [<span data-ttu-id="401c2-122">**deleteinstance**</span><span class="sxs-lookup"><span data-stu-id="401c2-122">**deleteinstance**</span></span>](pragma-deleteinstance.md) | <span data-ttu-id="401c2-123">Elimina una instancia existente de una clase del repositorio.</span><span class="sxs-lookup"><span data-stu-id="401c2-123">Deletes an existing instance of a class from the repository.</span></span>                                          |
| [<span data-ttu-id="401c2-124">**instanceflags**</span><span class="sxs-lookup"><span data-stu-id="401c2-124">**instanceflags**</span></span>](pragma-instanceflags.md)   | <span data-ttu-id="401c2-125">Controla la forma en que se crean o actualizan las instancias en función de las marcas especificadas.</span><span class="sxs-lookup"><span data-stu-id="401c2-125">Controls the way instances are created or updated depending on the flags specified.</span></span>                   |
| [<span data-ttu-id="401c2-126">**namespace**</span><span class="sxs-lookup"><span data-stu-id="401c2-126">**namespace**</span></span>](pragma-namespace.md)           | <span data-ttu-id="401c2-127">Solicita que el compilador cargue el archivo MOF en el espacio de nombres especificado como *namespacepath*.</span><span class="sxs-lookup"><span data-stu-id="401c2-127">Requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="401c2-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="401c2-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="401c2-129">Comandos de preprocesador</span><span class="sxs-lookup"><span data-stu-id="401c2-129">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



