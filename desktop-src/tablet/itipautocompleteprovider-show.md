---
description: Muestra u oculta la lista de autocompletar.
ms.assetid: 756ffa3d-03ee-4753-a826-3bc22ab16f5f
title: 'ITipAutocompleteProvider:: Show (método) (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.Show
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 950358ae28d1cb68af803ed6b7f520f1bbad8c03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818110"
---
# <a name="itipautocompleteprovidershow-method"></a><span data-ttu-id="c3967-103">ITipAutocompleteProvider:: Show (método)</span><span class="sxs-lookup"><span data-stu-id="c3967-103">ITipAutocompleteProvider::Show method</span></span>

<span data-ttu-id="c3967-104">Muestra u oculta la lista de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="c3967-104">Displays or hides the auto complete list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3967-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3967-105">Syntax</span></span>


```C++
HRESULT Show(
  [in] BOOL fShow
);
```



## <a name="parameters"></a><span data-ttu-id="c3967-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c3967-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3967-107">*fShow* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c3967-107">*fShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3967-108">**True** para mostrar la interfaz de usuario de autocompletar, **false** para ocultar la interfaz de usuario de la lista de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="c3967-108">**TRUE** to show the auto complete user interface, **FALSE** to hide the auto complete list user interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3967-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c3967-109">Return value</span></span>

<span data-ttu-id="c3967-110">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="c3967-110">This method can return one of these values.</span></span>



| <span data-ttu-id="c3967-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c3967-111">Return code</span></span>                                                                            | <span data-ttu-id="c3967-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3967-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="c3967-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c3967-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="c3967-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="c3967-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="c3967-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="c3967-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="c3967-116">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="c3967-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c3967-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3967-117">Remarks</span></span>

<span data-ttu-id="c3967-118">El cliente llama a este método para mostrar u ocultar la lista de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="c3967-118">This method is called by the client to show or hide the auto complete list.</span></span> <span data-ttu-id="c3967-119">Si no se muestra la lista Autocompletar y *fShow* es **false**, este método no hace nada.</span><span class="sxs-lookup"><span data-stu-id="c3967-119">If the auto complete list is not displayed and *fShow* is **FALSE**, this method does nothing.</span></span> <span data-ttu-id="c3967-120">Si se muestra la lista Autocompletar y *fShow* es **true**, este método no hace nada.</span><span class="sxs-lookup"><span data-stu-id="c3967-120">If the auto complete list is displayed and *fShow* is **TRUE**, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3967-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3967-121">Requirements</span></span>



| <span data-ttu-id="c3967-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3967-122">Requirement</span></span> | <span data-ttu-id="c3967-123">Value</span><span class="sxs-lookup"><span data-stu-id="c3967-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3967-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3967-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c3967-125">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c3967-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="c3967-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3967-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c3967-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c3967-127">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="c3967-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3967-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3967-129"><dt>TipAutoComplete. h (también requiere Peninputpanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c3967-129"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c3967-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c3967-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3967-131"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3967-131"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="c3967-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3967-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3967-133">**Interfaz ITipAutocompleteProvider**</span><span class="sxs-lookup"><span data-stu-id="c3967-133">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)
</dt> <dt>

[<span data-ttu-id="c3967-134">Referencia del panel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="c3967-134">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




