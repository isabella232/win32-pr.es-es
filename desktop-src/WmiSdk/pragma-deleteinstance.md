---
description: Elimina una instancia existente de una clase del repositorio.
ms.assetid: 4389f831-a60e-4198-a55a-79189d10a38a
ms.tgt_platform: multiple
title: pragma deleteinstance
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
ms.openlocfilehash: 10d4c735f1e59533b57ae1814cfb8e36b2c1ad76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082279"
---
# <a name="pragma-deleteinstance"></a><span data-ttu-id="50d83-103">pragma deleteinstance</span><span class="sxs-lookup"><span data-stu-id="50d83-103">pragma deleteinstance</span></span>

<span data-ttu-id="50d83-104">El comando **pragma deleteinstance** elimina una instancia existente de una clase del repositorio.</span><span class="sxs-lookup"><span data-stu-id="50d83-104">The **pragma deleteinstance** command deletes an existing instance of a class from the repository.</span></span>

<span data-ttu-id="50d83-105">A continuación se describe la sintaxis de este comando:</span><span class="sxs-lookup"><span data-stu-id="50d83-105">The following describes the syntax for this command:</span></span>


```mof
#pragma deleteinstance("InstanceId", [Flag])
```



<span data-ttu-id="50d83-106">*InstanceID* es un identificador único de la instancia que el compilador MOF elimina del espacio de nombres actual.</span><span class="sxs-lookup"><span data-stu-id="50d83-106">*InstanceId* is a unique identifier of the instance the MOF compiler deletes from the current namespace.</span></span>

<span data-ttu-id="50d83-107">La *\[ marca \]* debe ser uno de los argumentos siguientes.</span><span class="sxs-lookup"><span data-stu-id="50d83-107">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="50d83-108">Marca</span><span class="sxs-lookup"><span data-stu-id="50d83-108">Flag</span></span>   | <span data-ttu-id="50d83-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="50d83-109">Description</span></span>                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50d83-110">no superada</span><span class="sxs-lookup"><span data-stu-id="50d83-110">fail</span></span>   | <span data-ttu-id="50d83-111">Hace que el compilador MOF salga de un mensaje de error si la clase aún no existe en el repositorio.</span><span class="sxs-lookup"><span data-stu-id="50d83-111">Causes the MOF compiler to quit with an error message if the class does not already exist in the repository.</span></span> |
| <span data-ttu-id="50d83-112">nofail</span><span class="sxs-lookup"><span data-stu-id="50d83-112">nofail</span></span> | <span data-ttu-id="50d83-113">Hace que el compilador MOF continúe aunque la clase no exista todavía.</span><span class="sxs-lookup"><span data-stu-id="50d83-113">Causes the MOF compiler to continue even if the class does not already exist.</span></span>                                |



 

## <a name="examples"></a><span data-ttu-id="50d83-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="50d83-114">Examples</span></span>

<span data-ttu-id="50d83-115">En el ejemplo siguiente se muestra cómo usar este comando.</span><span class="sxs-lookup"><span data-stu-id="50d83-115">The following example shows how to use this command.</span></span>


```mof
#pragma deleteinstance(
    "MSFT_RisingFallingTemplate.id='TestRisingFallingCorrId'",
    nofail)
```



## <a name="requirements"></a><span data-ttu-id="50d83-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50d83-116">Requirements</span></span>



| <span data-ttu-id="50d83-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="50d83-117">Requirement</span></span> | <span data-ttu-id="50d83-118">Value</span><span class="sxs-lookup"><span data-stu-id="50d83-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="50d83-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50d83-119">Minimum supported client</span></span><br/> | <span data-ttu-id="50d83-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50d83-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="50d83-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50d83-121">Minimum supported server</span></span><br/> | <span data-ttu-id="50d83-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50d83-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50d83-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="50d83-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50d83-124">Comandos de preprocesador</span><span class="sxs-lookup"><span data-stu-id="50d83-124">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




