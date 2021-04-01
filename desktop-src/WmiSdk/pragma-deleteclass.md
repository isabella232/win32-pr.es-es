---
description: Elimina una clase existente y sus instancias del repositorio.
ms.assetid: 6f96d14a-16ab-4e83-a75f-5dbf162d1692
ms.tgt_platform: multiple
title: pragma deleteclass
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
ms.openlocfilehash: 0d3b5b1fa209be7fd472a87aec25a5e590d93c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913209"
---
# <a name="pragma-deleteclass"></a><span data-ttu-id="c03f4-103">pragma deleteclass</span><span class="sxs-lookup"><span data-stu-id="c03f4-103">pragma deleteclass</span></span>

<span data-ttu-id="c03f4-104">El comando de preprocesador **pragma deleteclass** elimina una clase existente y sus instancias del repositorio.</span><span class="sxs-lookup"><span data-stu-id="c03f4-104">The **pragma deleteclass** preprocessor command deletes an existing class and its instances from the repository.</span></span>

<span data-ttu-id="c03f4-105">A continuación se describe la sintaxis:</span><span class="sxs-lookup"><span data-stu-id="c03f4-105">The following describes the syntax:</span></span>


```mof
#pragma deleteclass("ClassName", [Flag])
```



<span data-ttu-id="c03f4-106">*ClassName* es el nombre de la clase que el compilador MOF elimina del espacio de nombres actual.</span><span class="sxs-lookup"><span data-stu-id="c03f4-106">*ClassName* is the name of the class that the MOF compiler deletes from the current namespace.</span></span>

<span data-ttu-id="c03f4-107">La *\[ marca \]* debe ser uno de los argumentos siguientes.</span><span class="sxs-lookup"><span data-stu-id="c03f4-107">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="c03f4-108">Marca</span><span class="sxs-lookup"><span data-stu-id="c03f4-108">Flag</span></span>   | <span data-ttu-id="c03f4-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c03f4-109">Description</span></span>                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c03f4-110">no superada</span><span class="sxs-lookup"><span data-stu-id="c03f4-110">fail</span></span>   | <span data-ttu-id="c03f4-111">Hace que el compilador MOF salga de un mensaje de error si la clase aún no existe en el repositorio.</span><span class="sxs-lookup"><span data-stu-id="c03f4-111">Causes the MOF compiler to quit with an error message if the class does not already exist in the repository.</span></span> |
| <span data-ttu-id="c03f4-112">nofail</span><span class="sxs-lookup"><span data-stu-id="c03f4-112">nofail</span></span> | <span data-ttu-id="c03f4-113">Hace que el compilador MOF continúe aunque la clase no exista todavía.</span><span class="sxs-lookup"><span data-stu-id="c03f4-113">Causes the MOF compiler to continue even if the class does not already exist.</span></span>                                |



 

## <a name="examples"></a><span data-ttu-id="c03f4-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c03f4-114">Examples</span></span>

<span data-ttu-id="c03f4-115">En el ejemplo siguiente se muestra cómo usar este comando.</span><span class="sxs-lookup"><span data-stu-id="c03f4-115">The following example shows how to use this command.</span></span>


```mof
#pragma deleteclass("MyClass1",FAIL)
```



## <a name="requirements"></a><span data-ttu-id="c03f4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c03f4-116">Requirements</span></span>



| <span data-ttu-id="c03f4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c03f4-117">Requirement</span></span> | <span data-ttu-id="c03f4-118">Value</span><span class="sxs-lookup"><span data-stu-id="c03f4-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c03f4-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c03f4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c03f4-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c03f4-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c03f4-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c03f4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c03f4-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c03f4-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c03f4-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c03f4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c03f4-124">Comandos de preprocesador</span><span class="sxs-lookup"><span data-stu-id="c03f4-124">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




