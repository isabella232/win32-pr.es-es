---
title: Usar C/C++-preprocesador con MIDL
description: El compilador MIDL no procesa los archivos de código fuente.
ms.assetid: 0f62d2a4-cfc3-42a7-b3a6-4e5c67c7c849
keywords:
- 'MIDL del compilador de MIDL, C: preprocesador'
- MIDL del preprocesador C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5752bd64ee9a9b5fc26d586b5bc33c1a1fb96e83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356994"
---
# <a name="using-cc-preprocessor-with-midl"></a><span data-ttu-id="7a8e8-105">Usar C/C++-preprocesador con MIDL</span><span class="sxs-lookup"><span data-stu-id="7a8e8-105">Using C/C++-Preprocessor with MIDL</span></span>

<span data-ttu-id="7a8e8-106">El compilador MIDL no procesa los archivos de código fuente.</span><span class="sxs-lookup"><span data-stu-id="7a8e8-106">The MIDL compiler does not preprocess source files.</span></span> <span data-ttu-id="7a8e8-107">En su lugar, el compilador MIDL usa un preprocesador disponible para preparar el flujo de entrada para el análisis.</span><span class="sxs-lookup"><span data-stu-id="7a8e8-107">Rather, the MIDL compiler uses an available preprocessor to prepare the input stream for parsing.</span></span> <span data-ttu-id="7a8e8-108">De forma predeterminada, MIDL utiliza el preprocesador para el compilador de C/C++ de Microsoft del mismo entorno de compilación que MIDL.</span><span class="sxs-lookup"><span data-stu-id="7a8e8-108">By default, MIDL uses the preprocessor for the Microsoft C/C++ compiler from the same building environment as MIDL.</span></span> <span data-ttu-id="7a8e8-109">El usuario puede indicar un preprocesador diferente que va a usar MIDL, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="7a8e8-109">The user can indicate a different preprocessor to be used by MIDL, if needed.</span></span>

<span data-ttu-id="7a8e8-110">MIDL genera ejecuciones de preprocesador independientes para los archivos IDL y ACF de nivel superior, así como para cada archivo importado con la Directiva de importación de MIDL.</span><span class="sxs-lookup"><span data-stu-id="7a8e8-110">MIDL spawns separate preprocessor runs for top-level IDL and ACF files, and for each file imported with the MIDL import directive.</span></span> <span data-ttu-id="7a8e8-111">El preprocesador controla directamente los archivos incluidos con la directiva **\# include** .</span><span class="sxs-lookup"><span data-stu-id="7a8e8-111">Files included with the **\#include** directive are handled by the preprocessor directly.</span></span>

<span data-ttu-id="7a8e8-112">En los temas siguientes se describen diversos aspectos de las interacciones del preprocesador de MIDL:</span><span class="sxs-lookup"><span data-stu-id="7a8e8-112">The following topics describe various aspects of MIDL-preprocessor interactions:</span></span>

-   [<span data-ttu-id="7a8e8-113">Requisitos del preprocesador de C para MIDL</span><span class="sxs-lookup"><span data-stu-id="7a8e8-113">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
-   [<span data-ttu-id="7a8e8-114">Comprobar las opciones del preprocesador</span><span class="sxs-lookup"><span data-stu-id="7a8e8-114">Verifying Preprocessor Options</span></span>](verifying-preprocessor-options.md)
-   [<span data-ttu-id="7a8e8-115">Guardar la salida del preprocesador</span><span class="sxs-lookup"><span data-stu-id="7a8e8-115">Saving Preprocessor Output</span></span>](saving-preprocessor-output.md)
-   [<span data-ttu-id="7a8e8-116">Trabajar con \# definiciones en archivos IDL</span><span class="sxs-lookup"><span data-stu-id="7a8e8-116">Dealing with \#defines in IDL Files</span></span>](dealing-with-defines-in-idl-files-2.md)

 

 




