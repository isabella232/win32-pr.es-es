---
description: Lo usa el cliente de Autocompletar para notificar a la aplicación el texto que un usuario ha tachado en el panel de entrada.
ms.assetid: 68413836-321a-4e75-8538-c5a8fc577c0f
title: 'ITipAutocompleteProvider:: UpdatePendingText (método) (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.UpdatePendingText
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 5c66e625639aa7088b1b3934a2f984d0f4097536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083450"
---
# <a name="itipautocompleteproviderupdatependingtext-method"></a><span data-ttu-id="40d89-103">ITipAutocompleteProvider:: UpdatePendingText (método)</span><span class="sxs-lookup"><span data-stu-id="40d89-103">ITipAutocompleteProvider::UpdatePendingText method</span></span>

<span data-ttu-id="40d89-104">Lo usa el cliente de Autocompletar para notificar a la aplicación el texto que un usuario ha tachado en el panel de entrada.</span><span class="sxs-lookup"><span data-stu-id="40d89-104">Used by the auto complete client to notify the application of the text a user has inked into Input Panel.</span></span>

## <a name="syntax"></a><span data-ttu-id="40d89-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40d89-105">Syntax</span></span>


```C++
HRESULT UpdatePendingText(
  [in] BSTR bstrPendingText
);
```



## <a name="parameters"></a><span data-ttu-id="40d89-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40d89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40d89-107">*bstrPendingText* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="40d89-107">*bstrPendingText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40d89-108">Texto de origen que se va a usar para generar la lista de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="40d89-108">Source text to be used to generate the auto complete list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40d89-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40d89-109">Return value</span></span>

<span data-ttu-id="40d89-110">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="40d89-110">This method can return one of these values.</span></span>



| <span data-ttu-id="40d89-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="40d89-111">Return code</span></span>                                                                            | <span data-ttu-id="40d89-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="40d89-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="40d89-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="40d89-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="40d89-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="40d89-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="40d89-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="40d89-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="40d89-116">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="40d89-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="40d89-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40d89-117">Remarks</span></span>

<span data-ttu-id="40d89-118">Este texto no contendrá el texto ya insertado en el campo con el foco.</span><span class="sxs-lookup"><span data-stu-id="40d89-118">This text will not contain the text already inserted in the focused field.</span></span> <span data-ttu-id="40d89-119">El proveedor de autocompletar es responsable de tener en cuenta el texto del campo actual y la selección para generar la lista de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="40d89-119">The auto complete provider is responsible for taking into account the current field text and the selection to generate the auto complete list.</span></span> <span data-ttu-id="40d89-120">Cuando *bstrPendingText* es **null**, la lista de autocompletar se genera con el texto actual a la izquierda de la selección en el campo.</span><span class="sxs-lookup"><span data-stu-id="40d89-120">When *bstrPendingText* is **NULL**, the auto complete list is generated with the current text to the left of the selection in the field.</span></span>

## <a name="requirements"></a><span data-ttu-id="40d89-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40d89-121">Requirements</span></span>



| <span data-ttu-id="40d89-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="40d89-122">Requirement</span></span> | <span data-ttu-id="40d89-123">Value</span><span class="sxs-lookup"><span data-stu-id="40d89-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40d89-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40d89-124">Minimum supported client</span></span><br/> | <span data-ttu-id="40d89-125">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="40d89-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="40d89-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40d89-126">Minimum supported server</span></span><br/> | <span data-ttu-id="40d89-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="40d89-127">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="40d89-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40d89-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="40d89-129"><dt>TipAutoComplete. h (también requiere Peninputpanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="40d89-129"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="40d89-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="40d89-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40d89-131"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40d89-131"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="40d89-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="40d89-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40d89-133">**Interfaz ITipAutocompleteProvider**</span><span class="sxs-lookup"><span data-stu-id="40d89-133">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)
</dt> <dt>

[<span data-ttu-id="40d89-134">Referencia del panel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="40d89-134">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




