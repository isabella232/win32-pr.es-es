---
title: Herramienta de Command-Line MkTypLib
description: MkTypLib es una aplicación de línea de comandos que procesa un archivo IDL para generar una biblioteca de tipos. También se puede utilizar para generar un archivo de encabezado de C o C++.
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc392351327124777c2d52d0bbe0653853dcb52
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794128"
---
# <a name="mktyplib-command-line-tool"></a><span data-ttu-id="f8145-104">Herramienta de Command-Line MkTypLib</span><span class="sxs-lookup"><span data-stu-id="f8145-104">MkTypLib Command-Line Tool</span></span>

<span data-ttu-id="f8145-105">\[La herramienta Mktyplib.exe está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="f8145-105">\[The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="f8145-106">En su lugar, utilice el compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="f8145-106">Use the MIDL compiler instead.</span></span> <span data-ttu-id="f8145-107">Si necesita compatibilidad con versiones anteriores de los programas de automatización anteriores, utilice el compilador MIDL con la opción **/mktyplib203** .\]</span><span class="sxs-lookup"><span data-stu-id="f8145-107">If you need backward compatibility with old Automation programs, use the MIDL compiler with the **/mktyplib203** option.\]</span></span>

<span data-ttu-id="f8145-108">MkTypLib es una aplicación de línea de comandos que procesa un archivo IDL para generar una biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="f8145-108">MkTypLib is a command-line application that processes an IDL file to produce a type library.</span></span> <span data-ttu-id="f8145-109">También se puede utilizar para generar un archivo de encabezado de C o C++.</span><span class="sxs-lookup"><span data-stu-id="f8145-109">It can also be used to generate a C or C++ header file.</span></span>

<span data-ttu-id="f8145-110">Para generar una biblioteca de tipos a partir de un archivo ODL:</span><span class="sxs-lookup"><span data-stu-id="f8145-110">To generate a type library from a ODL file:</span></span>

-   <span data-ttu-id="f8145-111">En el símbolo del sistema, ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="f8145-111">From the command prompt, run the following command:</span></span>

    <span data-ttu-id="f8145-112">\**mktyplibÂ \* \* \* nombreDeArchivo*</span><span class="sxs-lookup"><span data-stu-id="f8145-112">\**mktyplibÂ \*\*\*filename*</span></span>

    <span data-ttu-id="f8145-113">donde *filename* es el nombre del archivo ODL.</span><span class="sxs-lookup"><span data-stu-id="f8145-113">where *filename* is the name of the ODL file.</span></span>

<span data-ttu-id="f8145-114">MkTypLib también admite varios parámetros opcionales.</span><span class="sxs-lookup"><span data-stu-id="f8145-114">MkTypLib also supports several optional parameters.</span></span> <span data-ttu-id="f8145-115">Para obtener una lista completa, ejecute la siguiente línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="f8145-115">For a complete list, run the following command line:</span></span>

<span data-ttu-id="f8145-116">**MkTypLib/?**</span><span class="sxs-lookup"><span data-stu-id="f8145-116">**mktyplib /?**</span></span>

<span data-ttu-id="f8145-117">Dado que MkTypLib es una aplicación obsoleta, no puede analizar archivos IDL ni archivos con interfaces definidas fuera de una instrucción [**Library**](/windows/desktop/Midl/library) .</span><span class="sxs-lookup"><span data-stu-id="f8145-117">Because MkTypLib is an obsolete application, it cannot parse IDL files or files with interfaces defined outside of a [**library**](/windows/desktop/Midl/library) statement.</span></span> <span data-ttu-id="f8145-118">Para obtener más información, vea [diferencias entre MIDL y MkTypLib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).</span><span class="sxs-lookup"><span data-stu-id="f8145-118">For more information, see [Differences Between MIDL and MkTypLib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8145-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f8145-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8145-120">Traducir a C++</span><span class="sxs-lookup"><span data-stu-id="f8145-120">Translating to C++</span></span>](translating-to-c--.md)
</dt> </dl>

 

 