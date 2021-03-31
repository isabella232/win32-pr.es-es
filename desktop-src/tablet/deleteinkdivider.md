---
description: Elimina un objeto InkDivider y libera los recursos asociados.
ms.assetid: adf772e0-2829-4410-83c4-45a24bf3a848
title: DeleteInkDivider función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteInkDivider
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 8338d179b0bd57232463c794feca96885ee006fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912353"
---
# <a name="deleteinkdivider-function"></a><span data-ttu-id="1fe2f-103">DeleteInkDivider función)</span><span class="sxs-lookup"><span data-stu-id="1fe2f-103">DeleteInkDivider function</span></span>

<span data-ttu-id="1fe2f-104">Elimina un objeto [**InkDivider**](inkdivider-class.md) y libera los recursos asociados.</span><span class="sxs-lookup"><span data-stu-id="1fe2f-104">Deletes an [**InkDivider**](inkdivider-class.md) object and releases associated resources.</span></span>

<span data-ttu-id="1fe2f-105">Esta función no está pensada para ser utilizada por el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1fe2f-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fe2f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1fe2f-106">Syntax</span></span>


```C++
HRESULT WINAPI DeleteInkDivider(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a><span data-ttu-id="1fe2f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1fe2f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fe2f-108">*hDivider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1fe2f-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe2f-109">Identificador del objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="1fe2f-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fe2f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1fe2f-110">Return value</span></span>

<span data-ttu-id="1fe2f-111">Esta función puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="1fe2f-111">This function can return one of these values.</span></span>



| <span data-ttu-id="1fe2f-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1fe2f-112">Return code</span></span>                                                                                  | <span data-ttu-id="1fe2f-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="1fe2f-113">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="1fe2f-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1fe2f-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="1fe2f-115">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="1fe2f-115">The method succeeded.</span></span><br/>                |
| <dl> <span data-ttu-id="1fe2f-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1fe2f-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="1fe2f-117">El parámetro *hDivider* no es válido.</span><span class="sxs-lookup"><span data-stu-id="1fe2f-117">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1fe2f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fe2f-118">Requirements</span></span>



| <span data-ttu-id="1fe2f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fe2f-119">Requirement</span></span> | <span data-ttu-id="1fe2f-120">Value</span><span class="sxs-lookup"><span data-stu-id="1fe2f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1fe2f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fe2f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1fe2f-122">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1fe2f-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1fe2f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fe2f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1fe2f-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1fe2f-124">None supported</span></span><br/>                                                             |
| <span data-ttu-id="1fe2f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1fe2f-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="1fe2f-126"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fe2f-126"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




