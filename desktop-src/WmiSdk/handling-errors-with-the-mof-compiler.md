---
description: Si el compilador MOF no puede terminar de compilar un archivo MOF, el repositorio WMI puede quedar en un estado indefinido.
ms.assetid: 13adc666-6588-4cfd-a5eb-17da93434468
ms.tgt_platform: multiple
title: Control de errores con el compilador MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905b406020787de894a2821b501ee465ab63ea5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498118"
---
# <a name="handling-errors-with-the-mof-compiler"></a><span data-ttu-id="daadd-103">Control de errores con el compilador MOF</span><span class="sxs-lookup"><span data-stu-id="daadd-103">Handling Errors with the MOF Compiler</span></span>

<span data-ttu-id="daadd-104">Si el compilador MOF no puede terminar de compilar un archivo MOF, el repositorio WMI puede quedar en un estado indefinido.</span><span class="sxs-lookup"><span data-stu-id="daadd-104">If the MOF compiler cannot finish compiling a MOF file, the WMI repository may be left in an undefined state.</span></span> <span data-ttu-id="daadd-105">Por ejemplo, si está compilando un archivo MOF y usa el modificador de línea de comandos **-Class: createonly** , la compilación finaliza si ya existe una clase especificada en el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="daadd-105">For example, if you are compiling a MOF file and you use the **-class:createonly** command-line switch, the compilation terminates if a class specified in the MOF file already exists.</span></span> <span data-ttu-id="daadd-106">El compilador MOF almacena en el repositorio cualquier clase o instancia que se haya definido hasta el punto en el que se detiene el compilador.</span><span class="sxs-lookup"><span data-stu-id="daadd-106">The MOF compiler stores in the repository any classes or instances that were defined up to the point where the compiler stops.</span></span> <span data-ttu-id="daadd-107">En algunos casos, esto puede dejar el repositorio WMI en una condición no definida.</span><span class="sxs-lookup"><span data-stu-id="daadd-107">In some cases, this can leave the WMI repository in an undefined condition.</span></span>

<span data-ttu-id="daadd-108">En esta situación, es posible que necesite detener WMI, eliminar el repositorio WMI y hacer que WMI lo Recompile.</span><span class="sxs-lookup"><span data-stu-id="daadd-108">In this situation, you may need to stop WMI, delete the WMI repository, and have WMI rebuild it.</span></span> <span data-ttu-id="daadd-109">Todos los archivos MOF que contengan el comando [**pragma autocover**](pragma-autorecover.md) del [preprocesador](preprocessor-commands.md) se vuelven a generar cuando se reinicia WMI.</span><span class="sxs-lookup"><span data-stu-id="daadd-109">All MOF files that contain the [**pragma autorecover**](pragma-autorecover.md) [preprocessor command](preprocessor-commands.md) are rebuilt when WMI is restarted.</span></span> <span data-ttu-id="daadd-110">Debe volver a compilar manualmente cualquier archivo MOF que no incluya una `#pragma autorecover` instrucción.</span><span class="sxs-lookup"><span data-stu-id="daadd-110">You must manually recompile any MOF files that do not include a `#pragma autorecover` statement.</span></span>

<span data-ttu-id="daadd-111">Para obtener más información sobre cómo declarar clases e instancias con la sintaxis MOF, vea [diseñar clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="daadd-111">For more information about how to declare classes and instances using the MOF syntax, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="daadd-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="daadd-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="daadd-113">Compilar archivos MOF</span><span class="sxs-lookup"><span data-stu-id="daadd-113">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="daadd-114">**MOFCOMP**</span><span class="sxs-lookup"><span data-stu-id="daadd-114">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="daadd-115">Comandos de preprocesador</span><span class="sxs-lookup"><span data-stu-id="daadd-115">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



