---
description: Agrega un archivo MOF a la lista de archivos compilados durante la recuperación del repositorio.
ms.assetid: 8901c04e-f8c1-45b0-b69d-e2ebc948f088
ms.tgt_platform: multiple
title: Autorrecuperación de pragma
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9bb1cfca44e0bc5437d05d721ffcd57203e5aa9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002650"
---
# <a name="pragma-autorecover"></a><span data-ttu-id="e2458-103">Autorrecuperación de pragma</span><span class="sxs-lookup"><span data-stu-id="e2458-103">pragma autorecover</span></span>

<span data-ttu-id="e2458-104">El comando **pragma autocover** del preprocesador agrega un archivo MOF a la lista de archivos compilados durante la recuperación del repositorio.</span><span class="sxs-lookup"><span data-stu-id="e2458-104">The **pragma autorecover** preprocessor command adds a MOF file to the list of files compiled during repository recovery.</span></span> <span data-ttu-id="e2458-105">La lista de archivos MOF de **Autorrecuperación** se almacena en esta clave del registro:</span><span class="sxs-lookup"><span data-stu-id="e2458-105">The list of **autorecover** MOF files is stored in this registry key:</span></span>

<span data-ttu-id="e2458-106">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **autocover MOF**</span><span class="sxs-lookup"><span data-stu-id="e2458-106">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**autorecover mofs**</span></span>

<span data-ttu-id="e2458-107">WMI comprueba la integridad del repositorio WMI cuando el sistema operativo inicia WMI.</span><span class="sxs-lookup"><span data-stu-id="e2458-107">WMI checks the integrity of the WMI repository when the operating system starts WMI.</span></span> <span data-ttu-id="e2458-108">Si el repositorio está dañado, WMI vuelve a generar automáticamente el repositorio y vuelve a compilar los archivos MOF enumerados en esta clave en el registro.</span><span class="sxs-lookup"><span data-stu-id="e2458-108">If the repository is damaged, WMI automatically rebuilds the repository and recompiles any MOF files listed in this key in the registry.</span></span>

<span data-ttu-id="e2458-109">A continuación se describe la sintaxis del comando pragma autocover:</span><span class="sxs-lookup"><span data-stu-id="e2458-109">The following describes the syntax for the pragma autorecover command:</span></span>


```mof
#pragma autorecover
```



<span data-ttu-id="e2458-110">Sin embargo, debe observar las restricciones siguientes al usar este comando:</span><span class="sxs-lookup"><span data-stu-id="e2458-110">However, you must observe the following restrictions when using this command:</span></span>

-   <span data-ttu-id="e2458-111">WMI no puede recuperar archivos MOF ubicados en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="e2458-111">WMI cannot recover MOF files located on a remote computer.</span></span>

    <span data-ttu-id="e2458-112">Por lo tanto, los archivos MOF que se enumeran en esta clave del registro deben residir en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="e2458-112">Therefore, the MOF files listed in this registry key must reside on the local computer.</span></span>

-   <span data-ttu-id="e2458-113">No se pueden especificar los modificadores de línea de comandos que utiliza el compilador MOF cuando WMI recupera un archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="e2458-113">You cannot specify the command-line switches that the MOF compiler uses when WMI recovers a MOF file.</span></span>

    <span data-ttu-id="e2458-114">Por lo tanto, debe incluir comandos [pragma](-pragma.md) en el archivo MOF que hacen que los modificadores de línea de comandos no sean necesarios.</span><span class="sxs-lookup"><span data-stu-id="e2458-114">Therefore, you should include [pragma](-pragma.md) commands in your MOF file that make command-line switches unnecessary.</span></span> <span data-ttu-id="e2458-115">En el siguiente ejemplo se describe un modificador de la línea de comandos común que WMI no utiliza al recuperar un archivo MOF de esta clave del registro: **MOFCOMP-N:root \\ Test mymof. mof**</span><span class="sxs-lookup"><span data-stu-id="e2458-115">The following example describes a common command-line switch that WMI does not use when recovering a MOF file from this registry key: **mofcomp -N:Root\\Test mymof.mof**</span></span>

    <span data-ttu-id="e2458-116">Sin embargo, puede especificar el espacio de nombres mediante un comando [pragma](-pragma.md) en el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="e2458-116">However, you can specify the namespace using a [pragma](-pragma.md) command in the MOF file.</span></span>

    ```mof
    #pragma namespace ("\\\\.\\Root\\test")
    ```

    

## <a name="requirements"></a><span data-ttu-id="e2458-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2458-117">Requirements</span></span>



| <span data-ttu-id="e2458-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2458-118">Requirement</span></span> | <span data-ttu-id="e2458-119">Value</span><span class="sxs-lookup"><span data-stu-id="e2458-119">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e2458-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2458-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e2458-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2458-121">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e2458-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2458-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e2458-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2458-123">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2458-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2458-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2458-125">Comandos de preprocesador</span><span class="sxs-lookup"><span data-stu-id="e2458-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




