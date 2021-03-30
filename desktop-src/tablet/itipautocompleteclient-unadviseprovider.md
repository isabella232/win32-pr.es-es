---
description: Anula el registro del proveedor asociado.
ms.assetid: b5edc33d-dfd0-4350-b8cd-eaa30b726771
title: 'ITipAutocompleteClient:: UnadviseProvider (método) (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UnadviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 1100ebb700ef2fb769a13f9b62aacf5c1d007e0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910438"
---
# <a name="itipautocompleteclientunadviseprovider-method"></a><span data-ttu-id="65b7e-103">ITipAutocompleteClient:: UnadviseProvider (método)</span><span class="sxs-lookup"><span data-stu-id="65b7e-103">ITipAutocompleteClient::UnadviseProvider method</span></span>

<span data-ttu-id="65b7e-104">Anula el registro del proveedor asociado.</span><span class="sxs-lookup"><span data-stu-id="65b7e-104">Unregisters the associated provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="65b7e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65b7e-105">Syntax</span></span>


```C++
HRESULT UnadviseProvider(
  [in] HWND                   hWndField,
  [in] ITipAutocompleProvider *pIACProvider
);
```



## <a name="parameters"></a><span data-ttu-id="65b7e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65b7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65b7e-107">*hWndField* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65b7e-107">*hWndField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65b7e-108">Identificador de ventana del campo que proporciona la característica Autocompletar.</span><span class="sxs-lookup"><span data-stu-id="65b7e-108">Window handle of the field which provide the auto complete feature.</span></span>

</dd> <dt>

<span data-ttu-id="65b7e-109">*pIACProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65b7e-109">*pIACProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65b7e-110">Puntero de interfaz a la interfaz del proveedor de autocompletar cuya registro se va a anular.</span><span class="sxs-lookup"><span data-stu-id="65b7e-110">Interface pointer to the auto complete provider interface to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65b7e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65b7e-111">Return value</span></span>

<span data-ttu-id="65b7e-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="65b7e-112">This method can return one of these values.</span></span>



| <span data-ttu-id="65b7e-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="65b7e-113">Return code</span></span>                                                                            | <span data-ttu-id="65b7e-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="65b7e-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="65b7e-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="65b7e-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="65b7e-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="65b7e-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="65b7e-117"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="65b7e-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="65b7e-118">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="65b7e-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="65b7e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65b7e-119">Requirements</span></span>



| <span data-ttu-id="65b7e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="65b7e-120">Requirement</span></span> | <span data-ttu-id="65b7e-121">Value</span><span class="sxs-lookup"><span data-stu-id="65b7e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65b7e-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65b7e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="65b7e-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="65b7e-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="65b7e-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65b7e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="65b7e-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="65b7e-125">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="65b7e-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65b7e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="65b7e-127"><dt>TipAutoComplete. h (también requiere Peninputpanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="65b7e-127"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="65b7e-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="65b7e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65b7e-129"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65b7e-129"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="65b7e-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="65b7e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b7e-131">**Interfaz ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="65b7e-131">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="65b7e-132">Referencia del panel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="65b7e-132">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




