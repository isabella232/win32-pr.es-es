---
title: IEnumTfRenderingMarkup Clone (método)
description: El método Clone IEnumTfRenderingMarkup crea una copia del objeto de enumerador.
ms.assetid: f1b0ccf9-36d1-4eff-af7c-d7fb4f0e9104
keywords:
- Método Clone Text Services Framework
- Clone Method Text Services Framework, IEnumTfRenderingMarkup (interfaz)
- IEnumTfRenderingMarkup interface Text Services Framework, Clone (método)
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Clone
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f15d1bda18d2371f6518da4fa2884fac4df91b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685738"
---
# <a name="ienumtfrenderingmarkupclone-method"></a><span data-ttu-id="212c3-106">IEnumTfRenderingMarkup:: Clone (método)</span><span class="sxs-lookup"><span data-stu-id="212c3-106">IEnumTfRenderingMarkup::Clone method</span></span>

<span data-ttu-id="212c3-107">El método **IEnumTfRenderingMarkup:: Clone** crea una copia del objeto de enumerador.</span><span class="sxs-lookup"><span data-stu-id="212c3-107">The **IEnumTfRenderingMarkup::Clone** method creates a copy of the enumerator object.</span></span>

## <a name="syntax"></a><span data-ttu-id="212c3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="212c3-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="212c3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="212c3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="212c3-110">*ppEnum* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="212c3-110">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="212c3-111">\[\]un puntero a una interfaz [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) .</span><span class="sxs-lookup"><span data-stu-id="212c3-111">\[out\] A pointer to a [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="212c3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="212c3-112">Return value</span></span>

<span data-ttu-id="212c3-113">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="212c3-113">This method can return one of these values.</span></span>



| <span data-ttu-id="212c3-114">Value</span><span class="sxs-lookup"><span data-stu-id="212c3-114">Value</span></span>                                                                                        | <span data-ttu-id="212c3-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="212c3-115">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="212c3-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="212c3-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="212c3-117">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="212c3-117">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="212c3-118"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="212c3-118"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="212c3-119">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="212c3-119">An unspecified error occurred.</span></span><br/>      |
| <dl> <span data-ttu-id="212c3-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="212c3-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="212c3-121">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="212c3-121">One or more parameters are invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="212c3-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="212c3-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="212c3-123">Este método no está actualmente en los archivos de encabezado públicos.</span><span class="sxs-lookup"><span data-stu-id="212c3-123">This method is not currently in the public header files.</span></span> <span data-ttu-id="212c3-124">Para usar esta API, debe compilar MIDL en el [prototipo](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="212c3-124">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

