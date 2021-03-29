---
title: Errores y advertencias del compilador de MIDL
description: Al utilizar el compilador MIDL, los errores y las advertencias pueden deberse a un uso inadecuado de los modificadores de la línea de comandos o al contenido de los archivos IDL y ACF.
ms.assetid: 5c8d5a28-e559-4893-932f-b2306aefa932
keywords:
- Lenguaje de definición de interfaz de Microsoft MIDL, referencia
- MIDL del compilador MIDL, errores
- MIDL del compilador, errores
- errores MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae531528f83f3731b4449c7aba012f3228edd9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103902998"
---
# <a name="midl-compiler-errors-and-warnings"></a><span data-ttu-id="f723b-107">Errores y advertencias del compilador de MIDL</span><span class="sxs-lookup"><span data-stu-id="f723b-107">MIDL Compiler Errors and Warnings</span></span>

<span data-ttu-id="f723b-108">Al utilizar el compilador MIDL, los errores y las advertencias pueden deberse a un uso inadecuado de los modificadores de la línea de comandos o al contenido de los archivos IDL y ACF.</span><span class="sxs-lookup"><span data-stu-id="f723b-108">When using the MIDL compiler, errors and warnings can be caused by improper use of the command-line switches or by the content of the IDL and ACF files.</span></span> <span data-ttu-id="f723b-109">Si el error se debe a la entrada incorrecta de los modificadores de la línea de comandos, un mensaje de error o advertencia puede especificar el nombre de uno o varios modificadores de modo de compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="f723b-109">If the error is due to improperly entering the command-line switches, an error or warning message may specify the name of one or more MIDL compiler mode switches.</span></span> <span data-ttu-id="f723b-110">Por ejemplo, puede incluir ciertos atributos ACF en un archivo IDL al usar el modificador de **\_ configuración/App** , pero ese archivo IDL generará un error si se compila sin usar el modificador de **\_ configuración/App** .</span><span class="sxs-lookup"><span data-stu-id="f723b-110">For example, you can include certain ACF attributes in an IDL file when you use the /**app\_config** switch, but that IDL file will generate an error if you compile without using the /**app\_config** switch.</span></span>

<span data-ttu-id="f723b-111">Los errores de los archivos IDL y ACF se dividen en dos categorías: errores detectados por el preprocesador y errores reconocidos por el compilador.</span><span class="sxs-lookup"><span data-stu-id="f723b-111">Errors in the IDL and ACF files fall into two categories: errors caught by the preprocessor and errors recognized by the compiler.</span></span> <span data-ttu-id="f723b-112">En esta sección se enumeran los mensajes de error del compilador y el preprocesador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="f723b-112">This section lists the MIDL preprocessor and compiler error messages.</span></span> <span data-ttu-id="f723b-113">También se describen sus formatos y causas.</span><span class="sxs-lookup"><span data-stu-id="f723b-113">It also describes their formats and causes.</span></span>

-   [<span data-ttu-id="f723b-114">Formatos de mensajes de error y ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="f723b-114">Error and Warning Message Formats</span></span>](error-and-warning-message-formats.md)
-   [<span data-ttu-id="f723b-115">Errores de preprocesador</span><span class="sxs-lookup"><span data-stu-id="f723b-115">Preprocessor Errors</span></span>](preprocessor-errors.md)
-   [<span data-ttu-id="f723b-116">Errores del compilador</span><span class="sxs-lookup"><span data-stu-id="f723b-116">Compiler Errors</span></span>](compiler-errors.md)

 

 




