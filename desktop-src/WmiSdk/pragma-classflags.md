---
description: Controla la forma en que WMI crea o actualiza las clases según las marcas especificadas.
ms.assetid: ec535662-be14-44dc-ba0f-f9d2cbf630ea
ms.tgt_platform: multiple
title: pragma classflags
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
ms.openlocfilehash: 422185e3b1549d28e6d7004e2032675148d2408e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696670"
---
# <a name="pragma-classflags"></a><span data-ttu-id="c757d-103">pragma classflags</span><span class="sxs-lookup"><span data-stu-id="c757d-103">pragma classflags</span></span>

<span data-ttu-id="c757d-104">El comando de preprocesador **pragma classflags** controla la manera en que WMI crea o actualiza las clases según las marcas especificadas.</span><span class="sxs-lookup"><span data-stu-id="c757d-104">The **pragma classflags** preprocessor command controls the way WMI creates or updates classes depending on the flags specified.</span></span>

<span data-ttu-id="c757d-105">A continuación se describe la sintaxis de este comando:</span><span class="sxs-lookup"><span data-stu-id="c757d-105">The following describes the syntax for this command:</span></span>


```mof
#pragma classflags ("[flag1], [flag2]")
```



<span data-ttu-id="c757d-106">La *\[ marca \]* debe ser uno o varios de los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="c757d-106">*\[Flag\]* must be one or more of the following arguments.</span></span> <span data-ttu-id="c757d-107">Puede combinar las marcas que no se contradicen entre sí.</span><span class="sxs-lookup"><span data-stu-id="c757d-107">You can combine any flags that do not contradict each other.</span></span>



| <span data-ttu-id="c757d-108">Marca</span><span class="sxs-lookup"><span data-stu-id="c757d-108">Flag</span></span>        | <span data-ttu-id="c757d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c757d-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c757d-110">createonly</span><span class="sxs-lookup"><span data-stu-id="c757d-110">createonly</span></span>  | <span data-ttu-id="c757d-111">Indica al compilador que no realice ningún cambio en las clases existentes y finaliza una compilación si ya existe una clase especificada en el archivo MOF en WMI.</span><span class="sxs-lookup"><span data-stu-id="c757d-111">Instructs the compiler not make any changes to existing classes and terminates a compilation if a class specified in the MOF file already exists in WMI.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="c757d-112">Forza</span><span class="sxs-lookup"><span data-stu-id="c757d-112">forceupdate</span></span> | <span data-ttu-id="c757d-113">Fuerza la actualización de las clases cuando existen clases secundarias en conflicto.</span><span class="sxs-lookup"><span data-stu-id="c757d-113">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="c757d-114">Por ejemplo, si define un calificador de clase en una clase secundaria y la clase base intenta agregar el mismo calificador, el uso de esta marca hace que el compilador resuelva este conflicto eliminando el calificador en conflicto de la clase secundaria.</span><span class="sxs-lookup"><span data-stu-id="c757d-114">For example, if you define a class qualifier in a child class and the base class attempts to add the same qualifier, using this flag causes the compiler to resolve this conflict by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="c757d-115">Si la clase secundaria tiene instancias, se produce un error en la actualización.</span><span class="sxs-lookup"><span data-stu-id="c757d-115">If the child class has instances, the update fails.</span></span> |
| <span data-ttu-id="c757d-116">safeupdate</span><span class="sxs-lookup"><span data-stu-id="c757d-116">safeupdate</span></span>  | <span data-ttu-id="c757d-117">Permite al compilador actualizar clases incluso si existen clases secundarias, si el cambio no provoca conflictos con las clases secundarias.</span><span class="sxs-lookup"><span data-stu-id="c757d-117">Allows the compiler to update classes even if child classes exist, if the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="c757d-118">Por ejemplo, esta marca permite agregar una nueva propiedad a una clase base sin tener que agregar también la propiedad a cualquier clase secundaria existente previamente.</span><span class="sxs-lookup"><span data-stu-id="c757d-118">For example, this flag allows you to add a new property to a base class without also having to add the property to any pre-existing child class.</span></span> <span data-ttu-id="c757d-119">Si las clases secundarias tienen instancias, se produce un error en la actualización.</span><span class="sxs-lookup"><span data-stu-id="c757d-119">If the child classes have instances, the update fails.</span></span>                           |
| <span data-ttu-id="c757d-120">updateonly</span><span class="sxs-lookup"><span data-stu-id="c757d-120">updateonly</span></span>  | <span data-ttu-id="c757d-121">Indica al compilador que no cree ninguna clase nueva y hace que el compilador finalice la compilación si no existe una clase especificada en el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="c757d-121">Instructs the compiler to not create any new classes and causes the compiler to terminate the compilation if a class specified in the MOF file does not exist.</span></span>                                                                                                                                                                                                  |



 

## <a name="examples"></a><span data-ttu-id="c757d-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c757d-122">Examples</span></span>

<span data-ttu-id="c757d-123">En el ejemplo siguiente se muestra cómo usar este comando con las marcas updateonly y ForceUpdate.</span><span class="sxs-lookup"><span data-stu-id="c757d-123">The following example shows how to use this command with the updateonly and forceupdate flags.</span></span>


```mof
#pragma classflags ("updateonly", "forceupdate")
```



## <a name="requirements"></a><span data-ttu-id="c757d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c757d-124">Requirements</span></span>



| <span data-ttu-id="c757d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c757d-125">Requirement</span></span> | <span data-ttu-id="c757d-126">Value</span><span class="sxs-lookup"><span data-stu-id="c757d-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c757d-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c757d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c757d-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c757d-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c757d-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c757d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c757d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c757d-130">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c757d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="c757d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c757d-132">Comandos de preprocesador</span><span class="sxs-lookup"><span data-stu-id="c757d-132">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




