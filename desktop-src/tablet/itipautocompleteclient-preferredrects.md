---
description: Permite al cliente sugerir dónde colocar la lista de Autocompletar para evitar la superposición del panel de entrada.
ms.assetid: c82ffecb-f3e6-4c50-80bb-8393b39d3b2a
title: ITipAutocompleteClient::P método referredRects (TipAutoComplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.PreferredRects
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 04e935c668e858ae3d22936e8a63f9116ebd6ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716587"
---
# <a name="itipautocompleteclientpreferredrects-method"></a><span data-ttu-id="530c1-103">ITipAutocompleteClient::P método referredRects</span><span class="sxs-lookup"><span data-stu-id="530c1-103">ITipAutocompleteClient::PreferredRects method</span></span>

<span data-ttu-id="530c1-104">Permite al cliente sugerir dónde colocar la lista de Autocompletar para evitar la superposición del panel de entrada.</span><span class="sxs-lookup"><span data-stu-id="530c1-104">Allows the client to suggest where to position the auto complete list to avoid overlapping the Input Panel.</span></span>

## <a name="syntax"></a><span data-ttu-id="530c1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="530c1-105">Syntax</span></span>


```C++
HRESULT PreferredRects(
  [in]      RECT *prcACList,
  [in]      RECT *prcField,
  [out]     RECT *prcModified,
  [in, out] BOOL *pfShownAboveTip
);
```



## <a name="parameters"></a><span data-ttu-id="530c1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="530c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="530c1-107">*prcACList* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="530c1-107">*prcACList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="530c1-108">Rectángulo, en coordenadas de la pantalla, que indica la ubicación preferida del proveedor y el tamaño de la interfaz de usuario de la lista de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="530c1-108">A rectangle, in screen coordinates, indicating the provider's preferred location and the size of the auto complete list user interface.</span></span>

</dd> <dt>

<span data-ttu-id="530c1-109">*prcField* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="530c1-109">*prcField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="530c1-110">Rectángulo, en coordenadas de la pantalla, que indica la ubicación y el tamaño del campo con foco.</span><span class="sxs-lookup"><span data-stu-id="530c1-110">A rectangle, in screen coordinates, indicating the location and the size of the focused field.</span></span>

</dd> <dt>

<span data-ttu-id="530c1-111">*prcModified* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="530c1-111">*prcModified* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="530c1-112">Un rectángulo basado en el estado actual de la sugerencia y la ubicación y el tamaño de la lista de rellenado automático preferidos especificado por *prcACList*.</span><span class="sxs-lookup"><span data-stu-id="530c1-112">A rectangle based on the current state of the TIP and the preferred auto complete list location and size specified by *prcACList*.</span></span>

</dd> <dt>

<span data-ttu-id="530c1-113">*pfShownAboveTip* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="530c1-113">*pfShownAboveTip* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="530c1-114">**True** si el rectángulo modificado se va a mostrar sobre el área de destino del panel de entrada de texto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="530c1-114">**TRUE** if the modified rectangle is to be shown above the Text Input Panel's target area; otherwise, **FALSE**.</span></span> <span data-ttu-id="530c1-115">Este valor se debe inicializar en la orientación preferida del proveedor antes de que se llame al método.</span><span class="sxs-lookup"><span data-stu-id="530c1-115">This value must be initialized to the provider's preferred orientation before the method is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="530c1-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="530c1-116">Return value</span></span>

<span data-ttu-id="530c1-117">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="530c1-117">This method can return one of these values.</span></span>



| <span data-ttu-id="530c1-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="530c1-118">Return code</span></span>                                                                                  | <span data-ttu-id="530c1-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="530c1-119">Description</span></span>                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="530c1-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="530c1-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="530c1-121">Correcto.</span><span class="sxs-lookup"><span data-stu-id="530c1-121">Success.</span></span><br/>                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="530c1-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="530c1-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="530c1-123">Llame al [**método ITipAutocompleteClient:: RequestShowUI**](itipautocompleteclient-requestshowui.md) para establecer la ventana Lista de autocompletar emergente antes de llamar al [**método ITipAutocompleteClient::P referredrects**](itipautocompleteclient-preferredrects.md).</span><span class="sxs-lookup"><span data-stu-id="530c1-123">Call the [**ITipAutocompleteClient::RequestShowUI Method**](itipautocompleteclient-requestshowui.md) to set the popup auto complete list window before calling the [**ITipAutocompleteClient::PreferredRects Method**](itipautocompleteclient-preferredrects.md).</span></span><br/> |
| <dl> <span data-ttu-id="530c1-124"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="530c1-124"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="530c1-125">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="530c1-125">An unspecified error occurred.</span></span><br/>                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="530c1-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="530c1-126">Remarks</span></span>

<span data-ttu-id="530c1-127">Este es el método al que el proveedor de autocompletar llama cuando está a punto de mostrar la interfaz de usuario de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="530c1-127">This is the method that the auto complete provider calls when it is about to show the auto complete user interface.</span></span> <span data-ttu-id="530c1-128">El cliente modifica el rectángulo preferido del proveedor especificado por *prcACList* a través del argumento *prcModified* .</span><span class="sxs-lookup"><span data-stu-id="530c1-128">The client modifies the provider's preferred rectangle specified by *prcACList* through *prcModified* argument.</span></span>

<span data-ttu-id="530c1-129">Llame al [**método ITipAutocompleteClient:: RequestShowUI**](itipautocompleteclient-requestshowui.md) para establecer el identificador de la ventana Lista de rellenado automático emergente antes de llamar a **PreferredRects**.</span><span class="sxs-lookup"><span data-stu-id="530c1-129">Call the [**ITipAutocompleteClient::RequestShowUI Method**](itipautocompleteclient-requestshowui.md) to set the popup auto complete list window handle before you call **PreferredRects**.</span></span> <span data-ttu-id="530c1-130">Si no lo hace, se producirá un error de **E \_ INVALIDARG** al llamar a **PreferredRects**.</span><span class="sxs-lookup"><span data-stu-id="530c1-130">Failure to do so will cause an **E\_INVALIDARG** error when calling **PreferredRects**.</span></span>

## <a name="requirements"></a><span data-ttu-id="530c1-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="530c1-131">Requirements</span></span>



| <span data-ttu-id="530c1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="530c1-132">Requirement</span></span> | <span data-ttu-id="530c1-133">Value</span><span class="sxs-lookup"><span data-stu-id="530c1-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="530c1-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="530c1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="530c1-135">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="530c1-135">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="530c1-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="530c1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="530c1-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="530c1-137">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="530c1-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="530c1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="530c1-139"><dt>TipAutoComplete. h (también requiere Peninputpanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="530c1-139"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="530c1-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="530c1-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="530c1-141"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="530c1-141"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="530c1-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="530c1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="530c1-143">**Interfaz ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="530c1-143">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="530c1-144">**ITipAutocompleteClient:: RequestShowUI (método)**</span><span class="sxs-lookup"><span data-stu-id="530c1-144">**ITipAutocompleteClient::RequestShowUI Method**</span></span>](itipautocompleteclient-requestshowui.md)
</dt> <dt>

[<span data-ttu-id="530c1-145">Referencia del panel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="530c1-145">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




