---
description: Establece una función de devolución de llamada que se va a usar durante el reconocimiento de línea.
ms.assetid: 0b07ec80-328a-471b-b554-fa66f56a2871
title: SetLineRecoCallback función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineRecoCallback
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: b256a38d6d6ee6ecf43994c6619c369ea6ca2212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277392"
---
# <a name="setlinerecocallback-function"></a><span data-ttu-id="799f1-103">SetLineRecoCallback función)</span><span class="sxs-lookup"><span data-stu-id="799f1-103">SetLineRecoCallback function</span></span>

<span data-ttu-id="799f1-104">Establece una función de devolución de llamada que se va a usar durante el reconocimiento de línea.</span><span class="sxs-lookup"><span data-stu-id="799f1-104">Sets a callback function to be used during line recognition.</span></span>

<span data-ttu-id="799f1-105">Esta función auxiliar no está pensada para que la use el código de aplicación.</span><span class="sxs-lookup"><span data-stu-id="799f1-105">This helper function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="799f1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="799f1-106">Syntax</span></span>


```C++
HRESULT WINAPI SetLineRecoCallback(
  _In_ INT_PTR        hDivider,
       GetLineRecoDef pfn
);
```



## <a name="parameters"></a><span data-ttu-id="799f1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="799f1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="799f1-108">*hDivider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="799f1-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="799f1-109">Identificador del objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="799f1-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="799f1-110">*pfn*</span><span class="sxs-lookup"><span data-stu-id="799f1-110">*pfn*</span></span> 
</dt> <dd>

<span data-ttu-id="799f1-111">Puntero a una función a la que se llama cuando se produce el reconocimiento en el [**InkDivider**](inkdivider-class.md) que se pasa.</span><span class="sxs-lookup"><span data-stu-id="799f1-111">A pointer to a function that is called when recognition occurs on the [**InkDivider**](inkdivider-class.md) passed in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="799f1-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="799f1-112">Return value</span></span>

<span data-ttu-id="799f1-113">Esta función puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="799f1-113">This function can return one of these values.</span></span>



| <span data-ttu-id="799f1-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="799f1-114">Return code</span></span>                                                                                  | <span data-ttu-id="799f1-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="799f1-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="799f1-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="799f1-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="799f1-117">La función se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="799f1-117">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="799f1-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="799f1-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="799f1-119">El parámetro *pDivider* no es válido.</span><span class="sxs-lookup"><span data-stu-id="799f1-119">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="799f1-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="799f1-120">Remarks</span></span>

<span data-ttu-id="799f1-121">La siguiente es la sintaxis de la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="799f1-121">The following is the syntax for the callback function.</span></span>

``` syntax
public delegate void GetLineRecoDef(
        int cStrokes, 
        [MarshalAs(UnmanagedType.LPArray, ArraySubType = UnmanagedType.I4, SizeParamIndex = 0)]int [] aStrokeIds, 
        float degrees, 
        Point point, 
        [MarshalAs(UnmanagedType.BStr)] out string lineString, 
        out int cSegment, 
        out int[] strokeIdOrdered, 
        out int[] segmentStrokes,
        [MarshalAs(UnmanagedType.LPArray, ArraySubType = UnmanagedType.BStr)] out string [] aSegmentString
    );
```

## <a name="requirements"></a><span data-ttu-id="799f1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="799f1-122">Requirements</span></span>



| <span data-ttu-id="799f1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="799f1-123">Requirement</span></span> | <span data-ttu-id="799f1-124">Value</span><span class="sxs-lookup"><span data-stu-id="799f1-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="799f1-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="799f1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="799f1-126">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="799f1-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="799f1-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="799f1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="799f1-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="799f1-128">None supported</span></span><br/>                                                             |
| <span data-ttu-id="799f1-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="799f1-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="799f1-130"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="799f1-130"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




