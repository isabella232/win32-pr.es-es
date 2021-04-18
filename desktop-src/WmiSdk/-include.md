---
description: Incluye el contenido de un archivo MOF en otro archivo MOF.
ms.assetid: 06765956-e4ee-467b-9b3b-d5da17b9cd82
ms.tgt_platform: multiple
title: '#include'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5eb3d203cff5bca7e5096082cca7ba531580ae27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697646"
---
# <a name="include"></a><span data-ttu-id="52427-103">' #include '</span><span class="sxs-lookup"><span data-stu-id="52427-103">'#include'</span></span>
<span data-ttu-id="52427-104">/\* Title: MyMof. mof                           *//*   title: MyMof2. mof \*/</span><span class="sxs-lookup"><span data-stu-id="52427-104">/\*   Title: MyMof.Mof                           */ /*   Title: MyMof2.Mof                               \*/</span></span>

<span data-ttu-id="52427-105">El \# comando incluir preprocesador incluye el contenido de un archivo MOF en otro archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="52427-105">The \#include preprocessor command includes the contents of one MOF file into another MOF file.</span></span> <span data-ttu-id="52427-106">En el ejemplo de código siguiente se describe la sintaxis del \# comando include.</span><span class="sxs-lookup"><span data-stu-id="52427-106">The following code example describes the syntax for the \#include command.</span></span>

``` syntax
#include ("Moffile.mof")
```

<span data-ttu-id="52427-107">En el ejemplo anterior, Moffile. mof es el nombre del archivo MOF que se va a incluir.</span><span class="sxs-lookup"><span data-stu-id="52427-107">In the previous example, Moffile.mof is the name of the MOF file to include.</span></span>

<span data-ttu-id="52427-108">En el ejemplo siguiente se muestran dos archivos MOF.</span><span class="sxs-lookup"><span data-stu-id="52427-108">The following example shows two MOF files.</span></span> <span data-ttu-id="52427-109">Al compilar el primer archivo MOF, el compilador compila automáticamente el segundo archivo MOF (Mymof2. mof) en la ubicación donde se coloca la \# instrucción include.</span><span class="sxs-lookup"><span data-stu-id="52427-109">When you compile the first MOF file, the compiler automatically compiles the second MOF file (Mymof2.mof) in the location you place the \#include statement.</span></span>

``` syntax
/*   Title: MyMof.Mof                           */
/*                                              */ 
/*   This MOF file shows how to include  */
/*   an MOF file in another MOF file             */

#pragma namespace("\\\\.\\root")            

#include ("mymof2.mof")

class myclass1 
{
    [key] string Description;
};


instance of myclass1
{
    Description = "Description of myclass1";
};
/*   End of MyMof.Mof                           */
```

<span data-ttu-id="52427-110">El siguiente archivo MOF se incluye en el ejemplo anterior:</span><span class="sxs-lookup"><span data-stu-id="52427-110">The following MOF file is included in the previous example:</span></span>

``` syntax
/*   Title: MyMof2.Mof                               */
/*                                                   */
/*   This MOF is included when MyMof.MOF is compiled */

class myclass2 
{
    [key] string Description;
};


instance of myclass2
{
    Description = "Description of myclass2";
    
};
```

## <a name="related-topics"></a><span data-ttu-id="52427-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="52427-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52427-112">Comandos de preprocesador</span><span class="sxs-lookup"><span data-stu-id="52427-112">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



