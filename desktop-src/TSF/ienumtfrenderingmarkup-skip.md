---
title: IEnumTfRenderingMarkup SKIP (método)
description: El método SKIP de IEnumTfRenderingMarkup obtiene, desde la posición actual, el número especificado de elementos de la secuencia de enumeración.
ms.assetid: d328dfe3-36ab-4daf-8809-ad6686ca5dae
keywords:
- Skip Method Text Services Framework
- Skip Method Text Services Framework, IEnumTfRenderingMarkup (interfaz)
- IEnumTfRenderingMarkup interface Text Services Framework, SKIP (método)
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Skip
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3542893c739e6cfa2933d95bfed31f16957a0841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783707"
---
# <a name="ienumtfrenderingmarkupskip-method"></a><span data-ttu-id="b8358-106">IEnumTfRenderingMarkup:: Skip (método)</span><span class="sxs-lookup"><span data-stu-id="b8358-106">IEnumTfRenderingMarkup::Skip method</span></span>

<span data-ttu-id="b8358-107">El método **IEnumTfRenderingMarkup:: Skip** obtiene, desde la posición actual, el número especificado de elementos de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="b8358-107">The **IEnumTfRenderingMarkup::Skip** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8358-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8358-108">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG ulCount
);
```



## <a name="parameters"></a><span data-ttu-id="b8358-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8358-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8358-110">*ulCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8358-110">*ulCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8358-111">\[en \] especifica el número de elementos que se van a omitir.</span><span class="sxs-lookup"><span data-stu-id="b8358-111">\[in\] Specifies the number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8358-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8358-112">Return value</span></span>

<span data-ttu-id="b8358-113">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="b8358-113">This method can return one of these values.</span></span>



| <span data-ttu-id="b8358-114">Value</span><span class="sxs-lookup"><span data-stu-id="b8358-114">Value</span></span>                                                                                   | <span data-ttu-id="b8358-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8358-115">Description</span></span>                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b8358-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b8358-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="b8358-117">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b8358-117">The method was successful.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="b8358-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="b8358-118"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="b8358-119">El método llegó al final de la enumeración antes de que se pudiera omitir el número especificado de elementos.</span><span class="sxs-lookup"><span data-stu-id="b8358-119">The method reached the end of the enumeration before the specified number of elements could be skipped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b8358-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8358-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b8358-121">Este método no está actualmente en los archivos de encabezado públicos.</span><span class="sxs-lookup"><span data-stu-id="b8358-121">This method is not currently in the public header files.</span></span> <span data-ttu-id="b8358-122">Para usar esta API, debe compilar MIDL en el [prototipo](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="b8358-122">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 





