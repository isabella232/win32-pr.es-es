---
description: Comprueba si el objeto InkDivider puede usar la clase InkRecognizerContext para analizar palabras.
ms.assetid: fd848fcc-5258-401f-8b51-b9d57da173da
title: RecognizerContextSet función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizerContextSet
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 51e75b810c2103afed2e8ac8a28706b9c9af5da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910430"
---
# <a name="recognizercontextset-function"></a><span data-ttu-id="6081e-103">RecognizerContextSet función)</span><span class="sxs-lookup"><span data-stu-id="6081e-103">RecognizerContextSet function</span></span>

<span data-ttu-id="6081e-104">Comprueba si el objeto [**InkDivider**](inkdivider-class.md) puede usar la clase [**InkRecognizerContext**](inkrecognizercontext-class.md) para analizar palabras.</span><span class="sxs-lookup"><span data-stu-id="6081e-104">Tests whether the [**InkDivider**](inkdivider-class.md) object can use the [**InkRecognizerContext**](inkrecognizercontext-class.md) class to analyze words.</span></span>

<span data-ttu-id="6081e-105">Esta función no está pensada para ser utilizada por el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6081e-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6081e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6081e-106">Syntax</span></span>


```C++
HRESULT WINAPI RecognizerContextSet(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a><span data-ttu-id="6081e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6081e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6081e-108">*hDivider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6081e-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6081e-109">Identificador del objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="6081e-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6081e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6081e-110">Return value</span></span>

<span data-ttu-id="6081e-111">Esta función puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="6081e-111">This function can return one of these values.</span></span>



| <span data-ttu-id="6081e-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6081e-112">Return code</span></span>                                                                                  | <span data-ttu-id="6081e-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="6081e-113">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="6081e-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6081e-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6081e-115">La función se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="6081e-115">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="6081e-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6081e-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6081e-117">El parámetro *pDivider* no es válido.</span><span class="sxs-lookup"><span data-stu-id="6081e-117">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6081e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6081e-118">Requirements</span></span>



| <span data-ttu-id="6081e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6081e-119">Requirement</span></span> | <span data-ttu-id="6081e-120">Value</span><span class="sxs-lookup"><span data-stu-id="6081e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6081e-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6081e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6081e-122">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6081e-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="6081e-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6081e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6081e-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6081e-124">None supported</span></span><br/>                                                             |
| <span data-ttu-id="6081e-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6081e-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="6081e-126"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6081e-126"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




