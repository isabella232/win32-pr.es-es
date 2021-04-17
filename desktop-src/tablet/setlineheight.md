---
description: Establece la propiedad LineHeight en el objeto InkDivider.
ms.assetid: ce5e40c5-faa1-4d66-94f4-d5bd1a11ee4c
title: SetLineHeight función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineHeight
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: be4045e01ac890471536d95768668b633d8f2249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716450"
---
# <a name="setlineheight-function"></a><span data-ttu-id="2e3a6-103">SetLineHeight función)</span><span class="sxs-lookup"><span data-stu-id="2e3a6-103">SetLineHeight function</span></span>

<span data-ttu-id="2e3a6-104">Establece la propiedad [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) en el objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="2e3a6-104">Sets the [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) property on the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="2e3a6-105">Esta función auxiliar no está pensada para que la use el código de aplicación.</span><span class="sxs-lookup"><span data-stu-id="2e3a6-105">This helper function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e3a6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e3a6-106">Syntax</span></span>


```C++
HRESULT WINAPI SetLineHeight(
  _In_ INT_PTR hDivider,
  _In_ LONG    lLineHeight
);
```



## <a name="parameters"></a><span data-ttu-id="2e3a6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e3a6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e3a6-108">*hDivider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2e3a6-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e3a6-109">Identificador del objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="2e3a6-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="2e3a6-110">*lLineHeight* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2e3a6-110">*lLineHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e3a6-111">La propiedad [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) del objeto [**InkDivider**](inkdivider-class.md) , en unidades HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="2e3a6-111">The [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) property of the [**InkDivider**](inkdivider-class.md) object, in HIMETRIC units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e3a6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e3a6-112">Return value</span></span>

<span data-ttu-id="2e3a6-113">Esta función puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="2e3a6-113">This function can return one of these values.</span></span>



| <span data-ttu-id="2e3a6-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2e3a6-114">Return code</span></span>                                                                                  | <span data-ttu-id="2e3a6-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e3a6-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="2e3a6-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2e3a6-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="2e3a6-117">La función se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2e3a6-117">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="2e3a6-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2e3a6-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="2e3a6-119">El parámetro *pDivider* no es válido.</span><span class="sxs-lookup"><span data-stu-id="2e3a6-119">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2e3a6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e3a6-120">Requirements</span></span>



| <span data-ttu-id="2e3a6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e3a6-121">Requirement</span></span> | <span data-ttu-id="2e3a6-122">Value</span><span class="sxs-lookup"><span data-stu-id="2e3a6-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e3a6-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e3a6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2e3a6-124">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2e3a6-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="2e3a6-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e3a6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2e3a6-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2e3a6-126">None supported</span></span><br/>                                                             |
| <span data-ttu-id="2e3a6-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e3a6-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="2e3a6-128"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e3a6-128"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 
