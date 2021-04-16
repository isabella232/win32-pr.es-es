---
title: Llamadas a funciones
description: Llamadas a funciones
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- Aspectos de Windows Media Player, llamar a funciones en JScript
- máscaras, llamar a funciones en JScript
- llamar a funciones en JScript
- Archivos JScript para máscaras, llamar a funciones
- Aspectos de Windows Media Player, atributo scriptFile en JScript
- máscaras, atributo scriptFile en JScript
- atributos, scriptFile en JScript
- atributo scriptFile en JScript
- Archivos JScript para máscaras, atributo scriptFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9450c8ca09b75f66f6206c850a656192bb1bb9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532463"
---
# <a name="calling-functions"></a><span data-ttu-id="6af35-112">Llamadas a funciones</span><span class="sxs-lookup"><span data-stu-id="6af35-112">Calling Functions</span></span>

<span data-ttu-id="6af35-113">Si necesita llamar a más de unas pocas líneas de código, puede cargar un archivo de script mediante el atributo **scriptFile** del elemento **View** y llamar a las funciones del script.</span><span class="sxs-lookup"><span data-stu-id="6af35-113">If you need to call more than a few lines of code, you can load a script file using the **scriptFile** attribute of the **VIEW** element, and call the functions in the script.</span></span> <span data-ttu-id="6af35-114">Puede cargar más de un archivo por vista:</span><span class="sxs-lookup"><span data-stu-id="6af35-114">You can load more than one file per view:</span></span>


```C++
scriptFile = "myfile1.js;myfile2.js;myfile3.js"

```



<span data-ttu-id="6af35-115">Una vez cargados los archivos de script, puede llamar a funciones de dentro de la sección de vista.</span><span class="sxs-lookup"><span data-stu-id="6af35-115">After the script files are loaded, you can call functions in them from inside your View section.</span></span> <span data-ttu-id="6af35-116">Por ejemplo, para llamar a *una función llamada myFunction cuando se* haga clic en algo, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6af35-116">For example, to call a function called *myfunction* when something is clicked, type the following:</span></span>


```C++
onclick = "JScript: myfunction()"

```



> [!Note]  
> <span data-ttu-id="6af35-117">Si tiene más de una vista, solo las funciones de los archivos cargados en la vista actual estarán disponibles para el código XML y JScript que se ejecuta con la vista actual.</span><span class="sxs-lookup"><span data-stu-id="6af35-117">If you have more than one view, only the functions in files loaded into the current view are available to the XML and JScript code running with the current view.</span></span> <span data-ttu-id="6af35-118">Los archivos cargados en otras vistas no están en el ámbito de la vista actual.</span><span class="sxs-lookup"><span data-stu-id="6af35-118">Files loaded in other views are not in scope with the current view.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6af35-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6af35-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6af35-120">**Usar JScript**</span><span class="sxs-lookup"><span data-stu-id="6af35-120">**Using JScript**</span></span>](using-jscript.md)
</dt> </dl>

 

 




