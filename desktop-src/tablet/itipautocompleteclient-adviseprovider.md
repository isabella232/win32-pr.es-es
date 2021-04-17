---
description: Registra el proveedor con el cliente para permitir que el cliente llame al objeto de proveedor de autocompletar de la aplicación.
ms.assetid: 7b761b30-66f7-454a-9e0d-f45c8099f19f
title: 'ITipAutocompleteClient:: AdviseProvider (método) (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.AdviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 9ef35ac730089403ac47c14421de96e75a022192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716227"
---
# <a name="itipautocompleteclientadviseprovider-method"></a><span data-ttu-id="92058-103">ITipAutocompleteClient:: AdviseProvider (método)</span><span class="sxs-lookup"><span data-stu-id="92058-103">ITipAutocompleteClient::AdviseProvider method</span></span>

<span data-ttu-id="92058-104">Registra el proveedor con el cliente para permitir que el cliente llame al objeto de proveedor de autocompletar de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="92058-104">Registers the provider with the client to enable the client to call the application's auto complete provider object.</span></span>

## <a name="syntax"></a><span data-ttu-id="92058-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92058-105">Syntax</span></span>


```C++
HRESULT AdviseProvider(
  [in] HWND                     hWndField,
  [in] ITipAutocompleteProvider *pIACProvider
);
```



## <a name="parameters"></a><span data-ttu-id="92058-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92058-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92058-107">*hWndField* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92058-107">*hWndField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92058-108">Identificador de ventana del campo que proporciona la característica Autocompletar.</span><span class="sxs-lookup"><span data-stu-id="92058-108">The window handle of the field which provide the auto complete feature.</span></span>

</dd> <dt>

<span data-ttu-id="92058-109">*pIACProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92058-109">*pIACProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92058-110">Puntero de interfaz a la interfaz del proveedor de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="92058-110">The interface pointer to the auto complete provider interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92058-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92058-111">Return value</span></span>

<span data-ttu-id="92058-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="92058-112">This method can return one of these values.</span></span>



| <span data-ttu-id="92058-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="92058-113">Return code</span></span>                                                                            | <span data-ttu-id="92058-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="92058-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="92058-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="92058-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="92058-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="92058-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="92058-117"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="92058-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="92058-118">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="92058-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="92058-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92058-119">Requirements</span></span>



| <span data-ttu-id="92058-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="92058-120">Requirement</span></span> | <span data-ttu-id="92058-121">Value</span><span class="sxs-lookup"><span data-stu-id="92058-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92058-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92058-122">Minimum supported client</span></span><br/> | <span data-ttu-id="92058-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="92058-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="92058-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92058-124">Minimum supported server</span></span><br/> | <span data-ttu-id="92058-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="92058-125">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="92058-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92058-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="92058-127"><dt>TipAutoComplete. h (también requiere Peninputpanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="92058-127"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="92058-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="92058-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92058-129"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92058-129"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="92058-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="92058-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92058-131">**Interfaz ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="92058-131">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="92058-132">**ITipAutocompleteClient:: UnadviseProvider (método)**</span><span class="sxs-lookup"><span data-stu-id="92058-132">**ITipAutocompleteClient::UnadviseProvider Method**</span></span>](itipautocompleteclient-unadviseprovider.md)
</dt> <dt>

[<span data-ttu-id="92058-133">Referencia del panel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="92058-133">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




