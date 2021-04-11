---
description: Controla la forma en que se crean o actualizan las instancias en función de las marcas especificadas.
ms.assetid: 9932edf2-2e5f-4c5e-9889-f2be4af11bf2
ms.tgt_platform: multiple
title: pragma instanceflags
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
ms.openlocfilehash: acc05e201fcf153ab2156d4a360ce36b4539cd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279120"
---
# <a name="pragma-instanceflags"></a><span data-ttu-id="bf890-103">pragma instanceflags</span><span class="sxs-lookup"><span data-stu-id="bf890-103">pragma instanceflags</span></span>

<span data-ttu-id="bf890-104">El comando de preprocesador **pragma instanceflags** controla la manera en que se crean o actualizan las instancias en función de las marcas especificadas.</span><span class="sxs-lookup"><span data-stu-id="bf890-104">The **pragma instanceflags** preprocessor command controls the way instances are created or updated depending on the flags specified.</span></span>

<span data-ttu-id="bf890-105">A continuación se describe la sintaxis:</span><span class="sxs-lookup"><span data-stu-id="bf890-105">The following describes the syntax:</span></span>


```mof
#pragma instanceflags ([Flag])
```



<span data-ttu-id="bf890-106">La *\[ marca \]* debe ser uno de los argumentos siguientes.</span><span class="sxs-lookup"><span data-stu-id="bf890-106">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="bf890-107">Marca</span><span class="sxs-lookup"><span data-stu-id="bf890-107">Flag</span></span>       | <span data-ttu-id="bf890-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf890-108">Description</span></span>                                                                                                |
|------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf890-109">createonly</span><span class="sxs-lookup"><span data-stu-id="bf890-109">createonly</span></span> | <span data-ttu-id="bf890-110">Impide que el compilador cambie cualquier instancia existente en el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="bf890-110">Prevents the compiler from changing any existing instances in the MOF file.</span></span>                                |
| <span data-ttu-id="bf890-111">updateonly</span><span class="sxs-lookup"><span data-stu-id="bf890-111">updateonly</span></span> | <span data-ttu-id="bf890-112">Impide que el compilador cree nuevas instancias si no existe una instancia especificada en el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="bf890-112">Prevents the compiler from creating new instances if an instance specified in the MOF file does not exist.</span></span> |



 

## <a name="examples"></a><span data-ttu-id="bf890-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bf890-113">Examples</span></span>

<span data-ttu-id="bf890-114">En el ejemplo siguiente se muestra cómo usar este comando.</span><span class="sxs-lookup"><span data-stu-id="bf890-114">The following example shows how to use this command.</span></span>


```mof
#pragma instanceflags("createonly")
```



## <a name="requirements"></a><span data-ttu-id="bf890-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf890-115">Requirements</span></span>



| <span data-ttu-id="bf890-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf890-116">Requirement</span></span> | <span data-ttu-id="bf890-117">Value</span><span class="sxs-lookup"><span data-stu-id="bf890-117">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="bf890-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf890-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bf890-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf890-119">Windows Vista</span></span><br/>       |
| <span data-ttu-id="bf890-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf890-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bf890-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf890-121">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf890-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf890-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf890-123">Comandos de preprocesador</span><span class="sxs-lookup"><span data-stu-id="bf890-123">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




