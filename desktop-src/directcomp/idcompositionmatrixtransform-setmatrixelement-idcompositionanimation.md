---
title: IDCompositionMatrixTransform SetMatrixElement (int, int, IDCompositionAnimation)
description: Anima el valor de un elemento de la matriz de esta transformación 2D.
ms.assetid: 16A9E136-5F0C-4F34-A127-BF06C4530499
keywords:
- Método SetMatrixElement DirectComposition
- Método SetMatrixElement DirectComposition, interfaz IDCompositionMatrixTransform
- IDCompositionMatrixTransform interface DirectComposition, SetMatrixElement (método)
topic_type:
- apiref
api_name:
- IDCompositionMatrixTransform.SetMatrixElement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b4bf2a43e762b85b8b8cfd0c15468b3dc438221
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421147"
---
# <a name="idcompositionmatrixtransformsetmatrixelementint-int-idcompositionanimation-method"></a><span data-ttu-id="cb04a-106">Método IDCompositionMatrixTransform:: SetMatrixElement (int, int, IDCompositionAnimation \* )</span><span class="sxs-lookup"><span data-stu-id="cb04a-106">IDCompositionMatrixTransform::SetMatrixElement(int, int, IDCompositionAnimation\*) method</span></span>

<span data-ttu-id="cb04a-107">Anima el valor de un elemento de la matriz de esta transformación 2D.</span><span class="sxs-lookup"><span data-stu-id="cb04a-107">Animates the value of one element of the matrix of this 2D transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb04a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb04a-108">Syntax</span></span>


```C++
HRESULT SetMatrixElement(
  [in] int                    row,
  [in] int                    column,
  [in] IDCompositionAnimation *animation
);
```



## <a name="parameters"></a><span data-ttu-id="cb04a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb04a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb04a-110">*fila* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="cb04a-110">*row* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb04a-111">Índice de fila del elemento que se va a cambiar.</span><span class="sxs-lookup"><span data-stu-id="cb04a-111">The row index of the element to change.</span></span> <span data-ttu-id="cb04a-112">Este valor debe estar comprendido entre 0 y 2, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="cb04a-112">This value must be between 0 and 2, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="cb04a-113">*columna* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="cb04a-113">*column* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb04a-114">Índice de columna del elemento que se va a cambiar.</span><span class="sxs-lookup"><span data-stu-id="cb04a-114">The column index of the element to change.</span></span> <span data-ttu-id="cb04a-115">Este valor debe estar comprendido entre 0 y 1, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="cb04a-115">This value must be between 0 and 1, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="cb04a-116">*animación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="cb04a-116">*animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb04a-117">Animación que representa cómo cambia el valor del elemento especificado con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="cb04a-117">An animation that represents how the value of the specified element changes over time.</span></span> <span data-ttu-id="cb04a-118">Este parámetro no debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="cb04a-118">This parameter must not be NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb04a-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb04a-119">Return value</span></span>

<span data-ttu-id="cb04a-120">Si la función se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="cb04a-120">If the function succeeds, it returns S\_OK.</span></span> <span data-ttu-id="cb04a-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cb04a-121">Otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="cb04a-122">Consulte [códigos de error de DirectComposition](directcomposition-error-codes.md) para obtener una lista de códigos de error.</span><span class="sxs-lookup"><span data-stu-id="cb04a-122">See [DirectComposition Error Codes](directcomposition-error-codes.md) for a list of error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb04a-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb04a-123">Remarks</span></span>

<span data-ttu-id="cb04a-124">Este método realiza una copia de la animación especificada.</span><span class="sxs-lookup"><span data-stu-id="cb04a-124">This method makes a copy of the specified animation.</span></span> <span data-ttu-id="cb04a-125">Si el objeto al que hace referencia el parámetro *Animation* se cambia después de llamar a este método, el cambio no afecta al elemento a menos que se vuelva a llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="cb04a-125">If the object referenced by the *animation* parameter is changed after calling this method, the change does not affect the element unless this method is called again.</span></span> <span data-ttu-id="cb04a-126">Si el elemento se animaba previamente, al llamar a este método se reemplaza la animación anterior con la nueva animación.</span><span class="sxs-lookup"><span data-stu-id="cb04a-126">If the element was previously animated, calling this method replaces the previous animation with the new animation.</span></span>

<span data-ttu-id="cb04a-127">Este método produce un error si la *animación* es un puntero no válido o si no se creó con la misma interfaz [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) que la transformación afectada.</span><span class="sxs-lookup"><span data-stu-id="cb04a-127">This method fails if *animation* is an invalid pointer or if it was not created by the same [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) interface as the affected transform.</span></span> <span data-ttu-id="cb04a-128">La interfaz no puede ser una implementación personalizada; con este método solo se pueden usar las interfaces creadas por Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="cb04a-128">The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb04a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb04a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb04a-130">**IDCompositionMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="cb04a-130">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> </dl>

 

 