---
description: Notifica al panel de entrada que el usuario ha seleccionado algo en la lista de autocompletar y descartar todo el texto restante que todavía no se ha insertado.
ms.assetid: 2e6fabe1-7984-4908-bf90-0603d0dad268
title: 'ITipAutocompleteClient:: UserSelection (método) (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UserSelection
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 1894db9da3b8e3a36e59eb45150b27facfe0291f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716225"
---
# <a name="itipautocompleteclientuserselection-method"></a><span data-ttu-id="cc8e7-103">ITipAutocompleteClient:: UserSelection (método)</span><span class="sxs-lookup"><span data-stu-id="cc8e7-103">ITipAutocompleteClient::UserSelection method</span></span>

<span data-ttu-id="cc8e7-104">Notifica al panel de entrada que el usuario ha seleccionado algo en la lista de autocompletar y descartar todo el texto restante que todavía no se ha insertado.</span><span class="sxs-lookup"><span data-stu-id="cc8e7-104">Notifies the Input Panel that the user has selected something in the auto complete list and to discard all remaining text that has not yet been inserted.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc8e7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc8e7-105">Syntax</span></span>


```C++
HRESULT UserSelection();
```



## <a name="parameters"></a><span data-ttu-id="cc8e7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc8e7-106">Parameters</span></span>

<span data-ttu-id="cc8e7-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cc8e7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cc8e7-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc8e7-108">Return value</span></span>

<span data-ttu-id="cc8e7-109">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="cc8e7-109">This method can return one of these values.</span></span>



| <span data-ttu-id="cc8e7-110">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="cc8e7-110">Return code</span></span>                                                                            | <span data-ttu-id="cc8e7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc8e7-111">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="cc8e7-112"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="cc8e7-112"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="cc8e7-113">Correcto.</span><span class="sxs-lookup"><span data-stu-id="cc8e7-113">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="cc8e7-114"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="cc8e7-114"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="cc8e7-115">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="cc8e7-115">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cc8e7-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc8e7-116">Remarks</span></span>

<span data-ttu-id="cc8e7-117">Se llama a este método desde el proveedor para notificar al cliente que se ha realizado una selección por parte del usuario.</span><span class="sxs-lookup"><span data-stu-id="cc8e7-117">This method is called from the provider to notify the client that a selection has been made by the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc8e7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc8e7-118">Requirements</span></span>



| <span data-ttu-id="cc8e7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc8e7-119">Requirement</span></span> | <span data-ttu-id="cc8e7-120">Value</span><span class="sxs-lookup"><span data-stu-id="cc8e7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc8e7-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc8e7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cc8e7-122">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cc8e7-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="cc8e7-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc8e7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cc8e7-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cc8e7-124">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="cc8e7-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc8e7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc8e7-126"><dt>TipAutoComplete. h (también requiere Peninputpanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cc8e7-126"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cc8e7-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cc8e7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc8e7-128"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc8e7-128"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="cc8e7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc8e7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc8e7-130">**Interfaz ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="cc8e7-130">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="cc8e7-131">Referencia del panel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="cc8e7-131">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




