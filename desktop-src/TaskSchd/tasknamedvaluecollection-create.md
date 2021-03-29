---
title: TaskNamedValueCollection. Create (método)
description: En el caso de scripting, crea un par nombre-valor en la colección.
ms.assetid: f64e0548-fad3-4682-b50b-ff8ec685af36
keywords:
- Crear método Programador de tareas
- Create Method Programador de tareas, TaskNamedValueCollection Object
- Programador de tareas de objeto TaskNamedValueCollection, Create (método)
topic_type:
- apiref
api_name:
- TaskNamedValueCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3926142b25cbb2d65efaa45d6b767ce2e56ba86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492286"
---
# <a name="tasknamedvaluecollectioncreate-method"></a><span data-ttu-id="86754-106">TaskNamedValueCollection. Create (método)</span><span class="sxs-lookup"><span data-stu-id="86754-106">TaskNamedValueCollection.Create method</span></span>

<span data-ttu-id="86754-107">En el caso de scripting, crea un par nombre-valor en la colección.</span><span class="sxs-lookup"><span data-stu-id="86754-107">For scripting, creates a name-value pair in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="86754-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86754-108">Syntax</span></span>


```VB
TaskNamedValueCollection.Create( _
  ByVal name, _
  ByVal value, _
  ByRef pair _
)
```



## <a name="parameters"></a><span data-ttu-id="86754-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86754-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86754-110">*nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="86754-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86754-111">El nombre que está asociado a un valor en un par nombre-valor.</span><span class="sxs-lookup"><span data-stu-id="86754-111">The name that is associated with a value in a name-value pair.</span></span>

</dd> <dt>

<span data-ttu-id="86754-112">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="86754-112">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86754-113">Valor asociado a un nombre en un par nombre-valor.</span><span class="sxs-lookup"><span data-stu-id="86754-113">The value that is associated with a name in a name-value pair.</span></span>

</dd> <dt>

<span data-ttu-id="86754-114">*pareja* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="86754-114">*pair* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86754-115">Par nombre-valor que se crea en la colección.</span><span class="sxs-lookup"><span data-stu-id="86754-115">The name-value pair that is created in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86754-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86754-116">Return value</span></span>

<span data-ttu-id="86754-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="86754-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="86754-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86754-118">Requirements</span></span>



| <span data-ttu-id="86754-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="86754-119">Requirement</span></span> | <span data-ttu-id="86754-120">Value</span><span class="sxs-lookup"><span data-stu-id="86754-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86754-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86754-121">Minimum supported client</span></span><br/> | <span data-ttu-id="86754-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="86754-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="86754-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86754-123">Minimum supported server</span></span><br/> | <span data-ttu-id="86754-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="86754-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="86754-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="86754-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="86754-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="86754-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="86754-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="86754-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86754-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86754-128"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





