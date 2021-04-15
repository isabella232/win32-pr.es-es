---
title: Usar nuevos tipos de datos en el archivo IDL
description: El archivo de encabezado Basetsd. h define los nuevos tipos de datos necesarios para escribir aplicaciones que se ejecutan en Windows de 32 y 64 bits.
ms.assetid: 99a3904b-9120-4d1d-bd8c-1eb299bd6b27
keywords:
- Archivo de encabezado Basetsd. h 64 programación de Windows de bits
- tipos de datos en el archivo IDL 64 programación de Windows de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff1add2d70c99069911ac76ad168b7d31c3365f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714403"
---
# <a name="using-new-data-types-in-your-idl-file"></a><span data-ttu-id="89b93-105">Usar nuevos tipos de datos en el archivo IDL</span><span class="sxs-lookup"><span data-stu-id="89b93-105">Using New Data Types in Your IDL File</span></span>

<span data-ttu-id="89b93-106">El archivo de encabezado Basetsd. h define los nuevos tipos de datos necesarios para escribir aplicaciones que se ejecutan en Windows de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="89b93-106">The Basetsd.h header file defines the new data types needed for writing applications that run on both 32- and 64-bit Windows.</span></span> <span data-ttu-id="89b93-107">Para usar estos tipos de datos en las interfaces, importe Basetsd. h en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="89b93-107">To use these data types in your interfaces, import Basetsd.h into your IDL file.</span></span> <span data-ttu-id="89b93-108">No \# incluya el archivo o terminará con varias definiciones en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="89b93-108">Do not \#include the file or you will end up with multiple definitions at compile time.</span></span>

<span data-ttu-id="89b93-109">Como alternativa, puede incluir o importar el archivo Basetsd. idl en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="89b93-109">Alternatively, you can include or import the Basetsd.idl file into your IDL file.</span></span>

<span data-ttu-id="89b93-110">Para obtener más información sobre cómo agregar archivos de encabezado del sistema al archivo IDL, vea [importar archivos y bibliotecas de tipos](/windows/desktop/Midl/importing-files-and-type-libraries) e [importar archivos de encabezado del sistema](/windows/desktop/Midl/importing-system-header-files).</span><span class="sxs-lookup"><span data-stu-id="89b93-110">For more information on adding system header files to your IDL file, see [Importing Files and Type Libraries](/windows/desktop/Midl/importing-files-and-type-libraries) and [Importing System Header Files](/windows/desktop/Midl/importing-system-header-files).</span></span>

 

 