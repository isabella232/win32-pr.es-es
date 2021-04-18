---
description: Representa una lista de palabras que se pueden usar para mejorar el resultado del reconocimiento.
ms.assetid: d189fd13-ec69-45dc-8be4-fea48f337636
title: Clase InkWordList (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkWordList
- InkWordList.IInkWordList
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 7f3bbf077758bfd0449f5bca1ba3739342fa3658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707147"
---
# <a name="inkwordlist-class"></a><span data-ttu-id="5fbba-103">Clase InkWordList</span><span class="sxs-lookup"><span data-stu-id="5fbba-103">InkWordList class</span></span>

<span data-ttu-id="5fbba-104">Representa una lista de palabras que se pueden usar para mejorar el resultado del reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="5fbba-104">Represents a list of words that can be used to improve the recognition result.</span></span>

<span data-ttu-id="5fbba-105">**InkWordList** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5fbba-105">**InkWordList** has these types of members:</span></span>

-   [<span data-ttu-id="5fbba-106">Interfaces</span><span class="sxs-lookup"><span data-stu-id="5fbba-106">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="5fbba-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="5fbba-107">Methods</span></span>](#methods)

### <a name="interfaces"></a><span data-ttu-id="5fbba-108">Interfaces</span><span class="sxs-lookup"><span data-stu-id="5fbba-108">Interfaces</span></span>

<span data-ttu-id="5fbba-109">La clase **InkWordList** define estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="5fbba-109">The **InkWordList** class defines these interfaces.</span></span>



| <span data-ttu-id="5fbba-110">Interfaz</span><span class="sxs-lookup"><span data-stu-id="5fbba-110">Interface</span></span>        | <span data-ttu-id="5fbba-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fbba-111">Description</span></span>                                                           |
|:-----------------|:----------------------------------------------------------------------|
| <span data-ttu-id="5fbba-112">**IInkWordList**</span><span class="sxs-lookup"><span data-stu-id="5fbba-112">**IInkWordList**</span></span> | <span data-ttu-id="5fbba-113">Este objeto implementa la interfaz com **IInkWordList** .</span><span class="sxs-lookup"><span data-stu-id="5fbba-113">This object implements the **IInkWordList** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="5fbba-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="5fbba-114">Methods</span></span>

<span data-ttu-id="5fbba-115">La clase **InkWordList** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5fbba-115">The **InkWordList** class has these methods.</span></span>



| <span data-ttu-id="5fbba-116">Método</span><span class="sxs-lookup"><span data-stu-id="5fbba-116">Method</span></span>                                       | <span data-ttu-id="5fbba-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fbba-117">Description</span></span>                                                             |
|:---------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="5fbba-118">**AddWord**</span><span class="sxs-lookup"><span data-stu-id="5fbba-118">**AddWord**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-addword)       | <span data-ttu-id="5fbba-119">Agrega una sola palabra a **InkWordList**.</span><span class="sxs-lookup"><span data-stu-id="5fbba-119">Adds a single word to the **InkWordList**.</span></span><br/>                   |
| [<span data-ttu-id="5fbba-120">**Sin**</span><span class="sxs-lookup"><span data-stu-id="5fbba-120">**Merge**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-merge)           | <span data-ttu-id="5fbba-121">Combina otro **InkWordList** con en este **InkWordList**.</span><span class="sxs-lookup"><span data-stu-id="5fbba-121">Merges another **InkWordList** to into this **InkWordList**.</span></span><br/> |
| [<span data-ttu-id="5fbba-122">**RemoveWord**</span><span class="sxs-lookup"><span data-stu-id="5fbba-122">**RemoveWord**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-removeword) | <span data-ttu-id="5fbba-123">Quita una sola palabra de un **InkWordList**.</span><span class="sxs-lookup"><span data-stu-id="5fbba-123">Removes a single word from a **InkWordList**.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="5fbba-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5fbba-124">Remarks</span></span>

<span data-ttu-id="5fbba-125">Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.</span><span class="sxs-lookup"><span data-stu-id="5fbba-125">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fbba-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fbba-126">Requirements</span></span>



| <span data-ttu-id="5fbba-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fbba-127">Requirement</span></span> | <span data-ttu-id="5fbba-128">Value</span><span class="sxs-lookup"><span data-stu-id="5fbba-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fbba-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5fbba-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5fbba-130">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5fbba-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5fbba-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5fbba-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5fbba-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5fbba-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="5fbba-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5fbba-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fbba-134"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5fbba-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5fbba-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5fbba-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="5fbba-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fbba-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="5fbba-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="5fbba-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fbba-138">**Propiedad de la propiedad de palabras**</span><span class="sxs-lookup"><span data-stu-id="5fbba-138">**WordList Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)
</dt> <dt>

[<span data-ttu-id="5fbba-139">Constantes de Factoid</span><span class="sxs-lookup"><span data-stu-id="5fbba-139">Factoid Constants</span></span>](factoid-constants.md)
</dt> <dt>

[<span data-ttu-id="5fbba-140">**Clase InkRecognizerContext**</span><span class="sxs-lookup"><span data-stu-id="5fbba-140">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> </dl>

 

