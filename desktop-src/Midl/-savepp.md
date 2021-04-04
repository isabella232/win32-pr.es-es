---
title: modificador/savePP
description: Cuando se especifica la Directiva/savePP, el compilador MIDL no elimina el resultado del preprocesador de C/C++.
ms.assetid: 65a687a5-55ec-4e76-bcfc-38c0a317b85b
keywords:
- /savePP modificador MIDL
topic_type:
- apiref
api_name:
- /savePP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d3ab7032768cacfab6415548a09def453ab4f9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076767"
---
# <a name="savepp-switch"></a><span data-ttu-id="8c769-104">modificador/savePP</span><span class="sxs-lookup"><span data-stu-id="8c769-104">/savePP switch</span></span>

<span data-ttu-id="8c769-105">Cuando se especifica la directiva **/savePP** , el compilador MIDL no elimina el resultado del preprocesador de C/C++.</span><span class="sxs-lookup"><span data-stu-id="8c769-105">When the **/savePP** directive is specified, the MIDL compiler does not delete the output of the C/C++ preprocessor.</span></span>

``` syntax
midl /savePP
```

## <a name="switch-options"></a><span data-ttu-id="8c769-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="8c769-106">Switch Options</span></span>

<span data-ttu-id="8c769-107">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8c769-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c769-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c769-108">Remarks</span></span>

<span data-ttu-id="8c769-109">Este modificador permite a los desarrolladores discernir lo que está analizando el compilador de MIDL y es útil para la depuración.</span><span class="sxs-lookup"><span data-stu-id="8c769-109">This switch enables developers to discern what is being parsed by the MIDL compiler, and is useful for debugging.</span></span> <span data-ttu-id="8c769-110">La salida del preprocesador se escribe en uno o varios archivos temporales en el directorio indicado por la variable de entorno TEMP.</span><span class="sxs-lookup"><span data-stu-id="8c769-110">The output of the preprocessor is written to one or more temporary files in the directory indicated by the TEMP environment variable.</span></span> <span data-ttu-id="8c769-111">El nombre del archivo de salida o archivos sigue una Convención de nomenclatura de MID \* . tmp.</span><span class="sxs-lookup"><span data-stu-id="8c769-111">The name of the output file, or files, follows a naming convention of MID\*.tmp.</span></span> <span data-ttu-id="8c769-112">Tenga en cuenta que una sola compilación puede generar varios flujos de entrada preprocesados. Esto se debe a que la importación de un archivo IDL, en contraposición al uso de **\# include**, provoca una ejecución de preprocesador independiente.</span><span class="sxs-lookup"><span data-stu-id="8c769-112">Note that a single compile may generate several preprocessed input streams; this is because importing an IDL file, as opposed to using **\#include**, causes a separate preprocessor run.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c769-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c769-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c769-114">**/CPP \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="8c769-114">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="8c769-115">**/CPP \_ OPC**</span><span class="sxs-lookup"><span data-stu-id="8c769-115">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="8c769-116">/no \_ CPP,/nocpp</span><span class="sxs-lookup"><span data-stu-id="8c769-116">/no\_cpp, /nocpp</span></span>](-no-cpp-nocpp.md)
</dt> </dl>

 

 




