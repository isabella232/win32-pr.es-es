---
description: Un identificador HRECOWORDLIST se usa para administrar una lista de palabras que se adjunta a un contexto de reconocedor. Use una lista de palabras para mejorar los resultados del reconocimiento.
ms.assetid: 7333307b-1857-48a7-bb9f-bdbd8530f093
title: Identificador de HRECOWORDLIST (Resumen. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e5d33862cacb7040a26edc23d7db04c57206c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542123"
---
# <a name="hrecowordlist-handle"></a><span data-ttu-id="5d968-104">Identificador de HRECOWORDLIST</span><span class="sxs-lookup"><span data-stu-id="5d968-104">HRECOWORDLIST Handle</span></span>

<span data-ttu-id="5d968-105">Un identificador **HRECOWORDLIST** se usa para administrar una lista de palabras que se adjunta a un contexto de reconocedor.</span><span class="sxs-lookup"><span data-stu-id="5d968-105">An **HRECOWORDLIST** handle is used to manage a word list you attach to a recognizer context.</span></span> <span data-ttu-id="5d968-106">Use una lista de palabras para mejorar los resultados del reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="5d968-106">You use a word list to improve recognition results.</span></span>


```C++
typedef HANDLE HRECOWORDLIST;
```



## <a name="remarks"></a><span data-ttu-id="5d968-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d968-107">Remarks</span></span>

<span data-ttu-id="5d968-108">La siguiente función usa un **HRECOWORDLIST**.</span><span class="sxs-lookup"><span data-stu-id="5d968-108">The following function use an **HRECOWORDLIST**.</span></span>



| <span data-ttu-id="5d968-109">Función</span><span class="sxs-lookup"><span data-stu-id="5d968-109">Function</span></span>                                         | <span data-ttu-id="5d968-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d968-110">Description</span></span>                                         |
|--------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="5d968-111">**AddWordsToWordList**</span><span class="sxs-lookup"><span data-stu-id="5d968-111">**AddWordsToWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-addwordstowordlist) | <span data-ttu-id="5d968-112">Agrega una o más palabras a la lista de palabras.</span><span class="sxs-lookup"><span data-stu-id="5d968-112">Adds one or more words to the word list.</span></span><br/> |
| [<span data-ttu-id="5d968-113">**DestroyWordList**</span><span class="sxs-lookup"><span data-stu-id="5d968-113">**DestroyWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroywordlist)       | <span data-ttu-id="5d968-114">Destruye la lista de palabras actual.</span><span class="sxs-lookup"><span data-stu-id="5d968-114">Destroys the current word list.</span></span><br/>          |
| [<span data-ttu-id="5d968-115">**MakeWordList**</span><span class="sxs-lookup"><span data-stu-id="5d968-115">**MakeWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-makewordlist)             | <span data-ttu-id="5d968-116">Crea una lista de palabras.</span><span class="sxs-lookup"><span data-stu-id="5d968-116">Creates a word list.</span></span><br/>                     |



 

## <a name="requirements"></a><span data-ttu-id="5d968-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d968-117">Requirements</span></span>



| <span data-ttu-id="5d968-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d968-118">Requirement</span></span> | <span data-ttu-id="5d968-119">Value</span><span class="sxs-lookup"><span data-stu-id="5d968-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5d968-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d968-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5d968-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5d968-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="5d968-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d968-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5d968-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5d968-123">None supported</span></span><br/>                                                            |
| <span data-ttu-id="5d968-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d968-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d968-125"><dt>Resumen. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d968-125"><dt>Recapis.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d968-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d968-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d968-127">**SetWordList función)**</span><span class="sxs-lookup"><span data-stu-id="5d968-127">**SetWordList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 




