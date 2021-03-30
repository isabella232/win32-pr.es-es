---
description: Determina si el panel de entrada está listo para mostrar la lista de autocompletar.
ms.assetid: 1e0d4bc6-e6a3-4123-a381-00a41ed9c848
title: 'ITipAutocompleteClient:: RequestShowUI (método) (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.RequestShowUI
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: e547376bf2e9c50c224d1917e00329e8d9555e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277213"
---
# <a name="itipautocompleteclientrequestshowui-method"></a><span data-ttu-id="834c5-103">ITipAutocompleteClient:: RequestShowUI (método)</span><span class="sxs-lookup"><span data-stu-id="834c5-103">ITipAutocompleteClient::RequestShowUI method</span></span>

<span data-ttu-id="834c5-104">Determina si el panel de entrada está listo para mostrar la lista de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="834c5-104">Determines whether Input Panel is ready to have the auto complete list shown.</span></span>

## <a name="syntax"></a><span data-ttu-id="834c5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="834c5-105">Syntax</span></span>


```C++
HRESULT RequestShowUI(
  [in]  HWND hWndACList,
  [out] BOOL *pfAllowShowing
);
```



## <a name="parameters"></a><span data-ttu-id="834c5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="834c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="834c5-107">*hWndACList* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="834c5-107">*hWndACList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="834c5-108">Identificador de ventana de la interfaz de usuario de la lista de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="834c5-108">Window handle of the auto complete list user interface.</span></span>

</dd> <dt>

<span data-ttu-id="834c5-109">*pfAllowShowing* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="834c5-109">*pfAllowShowing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="834c5-110">**False** si el cliente recomienda no mostrar la interfaz de usuario de la lista de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="834c5-110">**FALSE** if client recommends to not show the auto complete list user interface.</span></span> <span data-ttu-id="834c5-111">**True** si el proveedor de autocompletar puede mostrar la interfaz de usuario de la lista.</span><span class="sxs-lookup"><span data-stu-id="834c5-111">**TRUE** if the auto complete provider can show the list user interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="834c5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="834c5-112">Return value</span></span>

<span data-ttu-id="834c5-113">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="834c5-113">This method can return one of these values.</span></span>



| <span data-ttu-id="834c5-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="834c5-114">Return code</span></span>                                                                            | <span data-ttu-id="834c5-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="834c5-115">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="834c5-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="834c5-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="834c5-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="834c5-117">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="834c5-118"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="834c5-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="834c5-119">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="834c5-119">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="834c5-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="834c5-120">Remarks</span></span>

<span data-ttu-id="834c5-121">El proveedor de autocompletar llama a este método cuando está a punto de mostrar la interfaz de usuario de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="834c5-121">This method is called by the auto complete provider when it is about to show the auto complete user interface.</span></span> <span data-ttu-id="834c5-122">Si el estado interno del cliente no permite al proveedor Mostrar la interfaz de usuario, *pfAllowShowing* se establecerá en **false**.</span><span class="sxs-lookup"><span data-stu-id="834c5-122">If the client's internal state doesn't allow the provider to show the user interface, *pfAllowShowing* will be set to **FALSE**.</span></span> <span data-ttu-id="834c5-123">Por ejemplo, cuando el texto se envía al campo desde la máscara de escritura a mano en el panel de entrada de Tablet PC y el usuario inicia inmediatamente el lápiz, el cliente recomienda no mostrar la interfaz de usuario de autocompletar, con el fin de evitar la destrucción del lápiz del usuario, estableciendo *pfAllowShowing* en **false**.</span><span class="sxs-lookup"><span data-stu-id="834c5-123">For example, when the text gets sent to the field from the handwriting skin on the Tablet PC Input Panel and the user immediately starts inking, the client will recommend to not show the auto complete user interface, in order to avoid destructing the user's inking, by setting *pfAllowShowing* to **FALSE**.</span></span>

<span data-ttu-id="834c5-124">Llame a **RequestShowUI** para establecer el identificador de la ventana Lista de autocompletar emergente antes de llamar al [**método referredrects de ITipAutocompleteClient::P**](itipautocompleteclient-preferredrects.md).</span><span class="sxs-lookup"><span data-stu-id="834c5-124">Call **RequestShowUI** to set the popup auto complete list window handle before you call the [**ITipAutocompleteClient::PreferredRects Method**](itipautocompleteclient-preferredrects.md).</span></span> <span data-ttu-id="834c5-125">Si no lo hace, se producirá un error de **E \_ INVALIDARG** al llamar a **PreferredRects**.</span><span class="sxs-lookup"><span data-stu-id="834c5-125">Failure to do so will cause an **E\_INVALIDARG** error when calling **PreferredRects**.</span></span>

## <a name="requirements"></a><span data-ttu-id="834c5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="834c5-126">Requirements</span></span>



| <span data-ttu-id="834c5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="834c5-127">Requirement</span></span> | <span data-ttu-id="834c5-128">Value</span><span class="sxs-lookup"><span data-stu-id="834c5-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="834c5-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="834c5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="834c5-130">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="834c5-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="834c5-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="834c5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="834c5-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="834c5-132">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="834c5-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="834c5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="834c5-134"><dt>TipAutoComplete. h (también requiere Peninputpanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="834c5-134"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="834c5-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="834c5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="834c5-136"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="834c5-136"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="834c5-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="834c5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="834c5-138">**Interfaz ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="834c5-138">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="834c5-139">**ITipAutocompleteClient::P método referredRects**</span><span class="sxs-lookup"><span data-stu-id="834c5-139">**ITipAutocompleteClient::PreferredRects Method**</span></span>](itipautocompleteclient-preferredrects.md)
</dt> <dt>

[<span data-ttu-id="834c5-140">Referencia del panel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="834c5-140">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




