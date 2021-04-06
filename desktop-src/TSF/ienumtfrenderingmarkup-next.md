---
title: Método Next IEnumTfRenderingMarkup
description: El siguiente método IEnumTfRenderingMarkup obtiene, desde la posición actual, el número especificado de elementos de la secuencia de enumeración.
ms.assetid: a3aec919-2c65-4e65-9430-d73fdaf5d28e
keywords:
- Next Method Text Services Framework
- Next Method Text Services Framework, IEnumTfRenderingMarkup (interfaz)
- IEnumTfRenderingMarkup interface Text Services Framework, Next (método)
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Next
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0989d35a2fa7c521d5ea103fbe40a73d012a3997
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078001"
---
# <a name="ienumtfrenderingmarkupnext-method"></a><span data-ttu-id="ac13b-106">IEnumTfRenderingMarkup:: Next (método)</span><span class="sxs-lookup"><span data-stu-id="ac13b-106">IEnumTfRenderingMarkup::Next method</span></span>

<span data-ttu-id="ac13b-107">El método **IEnumTfRenderingMarkup:: Next** obtiene, desde la posición actual, el número especificado de elementos de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="ac13b-107">The **IEnumTfRenderingMarkup::Next** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac13b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac13b-108">Syntax</span></span>


```C++
HRESULT Next(
  [out] ULONG ulCount,
  [out]       ppElement,
  [out] ULONG *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="ac13b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac13b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac13b-110">*ulCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ac13b-110">*ulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac13b-111">\[out \] especifica el número de elementos que se van a obtener.</span><span class="sxs-lookup"><span data-stu-id="ac13b-111">\[out\] Specifies the number of elements to obtain.</span></span>

</dd> <dt>

<span data-ttu-id="ac13b-112">*ppElement* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ac13b-112">*ppElement* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac13b-113">\[out \] puntero a una matriz de [estructuras \_ RENDERINGMARKUP de TF](/windows/desktop/TSF/tf-renderingmarkup) .</span><span class="sxs-lookup"><span data-stu-id="ac13b-113">\[out\] Pointer to an array of [TF\_RENDERINGMARKUP](/windows/desktop/TSF/tf-renderingmarkup) structures.</span></span> <span data-ttu-id="ac13b-114">Esta matriz debe tener al menos *ulCount* elementos de tamaño.</span><span class="sxs-lookup"><span data-stu-id="ac13b-114">This array must be at least *ulCount* elements in size.</span></span>

</dd> <dt>

<span data-ttu-id="ac13b-115">*pcFetched* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ac13b-115">*pcFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac13b-116">\[out \] puntero a un valor ulong que recibe el número de elementos obtenidos realmente.</span><span class="sxs-lookup"><span data-stu-id="ac13b-116">\[out\] Pointer to a ULONG value that receives the number of elements actually obtained.</span></span> <span data-ttu-id="ac13b-117">Este valor puede ser menor que el número de elementos solicitados.</span><span class="sxs-lookup"><span data-stu-id="ac13b-117">This value can be less than the number of items requested.</span></span> <span data-ttu-id="ac13b-118">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ac13b-118">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac13b-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac13b-119">Return value</span></span>

<span data-ttu-id="ac13b-120">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="ac13b-120">This method can return one of these values.</span></span>



| <span data-ttu-id="ac13b-121">Value</span><span class="sxs-lookup"><span data-stu-id="ac13b-121">Value</span></span>                                                                                        | <span data-ttu-id="ac13b-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac13b-122">Description</span></span>                                                                                                         |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ac13b-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ac13b-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ac13b-124">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ac13b-124">The method was successful.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="ac13b-125"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="ac13b-125"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="ac13b-126">El método llegó al final de la enumeración antes de que se pudiera obtener el número especificado de elementos.</span><span class="sxs-lookup"><span data-stu-id="ac13b-126">The method reached the end of the enumeration before the specified number of elements could be obtained.</span></span><br/> |
| <dl> <span data-ttu-id="ac13b-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ac13b-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ac13b-128">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="ac13b-128">One or more parameters are invalid.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="ac13b-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac13b-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ac13b-130">Este método no está actualmente en los archivos de encabezado públicos.</span><span class="sxs-lookup"><span data-stu-id="ac13b-130">This method is not currently in the public header files.</span></span> <span data-ttu-id="ac13b-131">Para usar esta API, debe compilar MIDL en el [prototipo](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="ac13b-131">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

