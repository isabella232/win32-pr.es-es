---
description: Las siguientes clases se declaran y asocian a los identificadores de clase (CLSID) en wmcodecdsp. h.
ms.assetid: f82d92dc-fbce-4274-a10f-72fa8dd776cc
title: Identificadores de clase para el analizador de tabla de contenido (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5108855c687085e77ce36aa14b3424732e25572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677253"
---
# <a name="class-identifiers-for-table-of-contents-parser"></a><span data-ttu-id="d8538-103">Identificadores de clase para el analizador de tabla de contenido</span><span class="sxs-lookup"><span data-stu-id="d8538-103">Class Identifiers for Table of Contents Parser</span></span>

<span data-ttu-id="d8538-104">Las siguientes clases se declaran y asocian a los identificadores de clase (CLSID) en wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="d8538-104">The following classes are declared and associated with class identifiers (CLSIDs) in wmcodecdsp.h.</span></span>



| <span data-ttu-id="d8538-105">Nombre de la clase</span><span class="sxs-lookup"><span data-stu-id="d8538-105">Class name</span></span>       | <span data-ttu-id="d8538-106">Nombre descriptivo del objeto</span><span class="sxs-lookup"><span data-stu-id="d8538-106">Friendly object name</span></span> |
|------------------|----------------------|
| <span data-ttu-id="d8538-107">CTocEntry</span><span class="sxs-lookup"><span data-stu-id="d8538-107">CTocEntry</span></span>        | <span data-ttu-id="d8538-108">Entrada de TDC</span><span class="sxs-lookup"><span data-stu-id="d8538-108">TOC Entry</span></span>            |
| <span data-ttu-id="d8538-109">CTocEntryList</span><span class="sxs-lookup"><span data-stu-id="d8538-109">CTocEntryList</span></span>    | <span data-ttu-id="d8538-110">Lista de entradas de TDC</span><span class="sxs-lookup"><span data-stu-id="d8538-110">TOC Entry List</span></span>       |
| <span data-ttu-id="d8538-111">CToc</span><span class="sxs-lookup"><span data-stu-id="d8538-111">CToc</span></span>             | <span data-ttu-id="d8538-112">TABLA DE CONTENIDO</span><span class="sxs-lookup"><span data-stu-id="d8538-112">TOC</span></span>                  |
| <span data-ttu-id="d8538-113">CTocCollection</span><span class="sxs-lookup"><span data-stu-id="d8538-113">CTocCollection</span></span>   | <span data-ttu-id="d8538-114">Colección TOC</span><span class="sxs-lookup"><span data-stu-id="d8538-114">TOC Collection</span></span>       |
| <span data-ttu-id="d8538-115">CTocParser</span><span class="sxs-lookup"><span data-stu-id="d8538-115">CTocParser</span></span>       | <span data-ttu-id="d8538-116">Analizador de TDC</span><span class="sxs-lookup"><span data-stu-id="d8538-116">TOC Parser</span></span>           |
| <span data-ttu-id="d8538-117">CTocGeneratorDmo</span><span class="sxs-lookup"><span data-stu-id="d8538-117">CTocGeneratorDmo</span></span> | <span data-ttu-id="d8538-118">Generador de TDC</span><span class="sxs-lookup"><span data-stu-id="d8538-118">TOC Generator</span></span>        |



 

<span data-ttu-id="d8538-119">En la tabla anterior se proporciona un nombre de objeto descriptivo para cada clase.</span><span class="sxs-lookup"><span data-stu-id="d8538-119">The preceding table gives a friendly object name for each class.</span></span> <span data-ttu-id="d8538-120">En esta documentación se usan esos nombres descriptivos para hacer referencia a las instancias de las clases.</span><span class="sxs-lookup"><span data-stu-id="d8538-120">This documentation uses those friendly names to refer to instances of the classes.</span></span> <span data-ttu-id="d8538-121">Por ejemplo, la documentación hace referencia a una instancia de la clase CTocEntry como un objeto de entrada de TDC.</span><span class="sxs-lookup"><span data-stu-id="d8538-121">For example, the documentation refers to an instance of the CTocEntry class as a TOC Entry object.</span></span>

<span data-ttu-id="d8538-122">En el código, puede usar **\_ \_ uuidof** para hacer referencia a los CLSID.</span><span class="sxs-lookup"><span data-stu-id="d8538-122">In code, you can use **\_\_uuidof** to refer to the CLSIDs.</span></span> <span data-ttu-id="d8538-123">Por ejemplo, puede usar el código siguiente para hacer referencia al CLSID de CTocGeneratorDmo.</span><span class="sxs-lookup"><span data-stu-id="d8538-123">For example, you can use the following code to refer to the CLSID for CTocGeneratorDmo.</span></span>


```C++
__uuidof(CTocGeneratorDmo)
```



### <a name="clsid-constants-defined-in-wmcodecdsph"></a><span data-ttu-id="d8538-124">Constantes CLSID definidas en Wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="d8538-124">CLSID Constants Defined in Wmcodecdsp.h</span></span>

<span data-ttu-id="d8538-125">Como alternativa al uso de **\_ \_ uuidof**, puede usar constantes para hacer referencia a los CLSID.</span><span class="sxs-lookup"><span data-stu-id="d8538-125">As an alternative to using **\_\_uuidof**, you can use constants to refer to the CLSIDs.</span></span> <span data-ttu-id="d8538-126">Las siguientes constantes se definen en wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="d8538-126">The following constants are defined in wmcodecdsp.h</span></span>



| <span data-ttu-id="d8538-127">Nombre de la clase</span><span class="sxs-lookup"><span data-stu-id="d8538-127">Class name</span></span>     | <span data-ttu-id="d8538-128">Constante CLSID</span><span class="sxs-lookup"><span data-stu-id="d8538-128">CLSID constant</span></span>        |
|----------------|-----------------------|
| <span data-ttu-id="d8538-129">CTocEntry</span><span class="sxs-lookup"><span data-stu-id="d8538-129">CTocEntry</span></span>      | <span data-ttu-id="d8538-130">CLSID \_ CTocEntry</span><span class="sxs-lookup"><span data-stu-id="d8538-130">CLSID\_CTocEntry</span></span>      |
| <span data-ttu-id="d8538-131">CTocEntryList</span><span class="sxs-lookup"><span data-stu-id="d8538-131">CTocEntryList</span></span>  | <span data-ttu-id="d8538-132">CLSID \_ CTocEntryList</span><span class="sxs-lookup"><span data-stu-id="d8538-132">CLSID\_CTocEntryList</span></span>  |
| <span data-ttu-id="d8538-133">CToc</span><span class="sxs-lookup"><span data-stu-id="d8538-133">CToc</span></span>           | <span data-ttu-id="d8538-134">CLSID \_ CToc</span><span class="sxs-lookup"><span data-stu-id="d8538-134">CLSID\_CToc</span></span>           |
| <span data-ttu-id="d8538-135">CTocCollection</span><span class="sxs-lookup"><span data-stu-id="d8538-135">CTocCollection</span></span> | <span data-ttu-id="d8538-136">CLSID \_ CTocCollection</span><span class="sxs-lookup"><span data-stu-id="d8538-136">CLSID\_CTocCollection</span></span> |
| <span data-ttu-id="d8538-137">CTocParser</span><span class="sxs-lookup"><span data-stu-id="d8538-137">CTocParser</span></span>     | <span data-ttu-id="d8538-138">CLSID \_ CTocParser</span><span class="sxs-lookup"><span data-stu-id="d8538-138">CLSID\_CTocParser</span></span>     |



 

### <a name="clsid-constants-defined-in-wmcodecdspuuidlib"></a><span data-ttu-id="d8538-139">Constantes CLSID definidas en Wmcodecdspuuid. lib</span><span class="sxs-lookup"><span data-stu-id="d8538-139">CLSID Constants Defined in Wmcodecdspuuid.lib</span></span>

<span data-ttu-id="d8538-140">La siguiente constante CLSID se declara, pero no se define, en wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="d8538-140">The following CLSID constant is declared, but not defined, in wmcodecdsp.h.</span></span> <span data-ttu-id="d8538-141">Para usarlo en el código, debe vincular a wmcodecdspuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d8538-141">To use it in code, you must link against wmcodecdspuuid.lib.</span></span>



| <span data-ttu-id="d8538-142">Nombre de la clase</span><span class="sxs-lookup"><span data-stu-id="d8538-142">Class name</span></span>       | <span data-ttu-id="d8538-143">Constante CLSID</span><span class="sxs-lookup"><span data-stu-id="d8538-143">CLSID constant</span></span>          |
|------------------|-------------------------|
| <span data-ttu-id="d8538-144">CTocGeneratorDmo</span><span class="sxs-lookup"><span data-stu-id="d8538-144">CTocGeneratorDmo</span></span> | <span data-ttu-id="d8538-145">CLSID \_ CTocGeneratorDmo</span><span class="sxs-lookup"><span data-stu-id="d8538-145">CLSID\_CTocGeneratorDmo</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d8538-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8538-146">Requirements</span></span>



| <span data-ttu-id="d8538-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8538-147">Requirement</span></span> | <span data-ttu-id="d8538-148">Value</span><span class="sxs-lookup"><span data-stu-id="d8538-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8538-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8538-149">Minimum supported client</span></span><br/> | <span data-ttu-id="d8538-150">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d8538-150">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d8538-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8538-151">Minimum supported server</span></span><br/> | <span data-ttu-id="d8538-152">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d8538-152">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d8538-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8538-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8538-154"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8538-154"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="d8538-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d8538-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8538-156"><dt>Wmvdspa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8538-156"><dt>Wmvdspa.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d8538-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8538-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8538-158">Objetos de analizador de tabla de contenido</span><span class="sxs-lookup"><span data-stu-id="d8538-158">Table of Contents Parser Objects</span></span>](toc-parser-objects.md)
</dt> </dl>

 

 




