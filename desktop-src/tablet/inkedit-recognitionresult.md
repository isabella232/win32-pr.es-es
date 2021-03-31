---
description: 'Se produce cuando el control InkEdit obtiene los resultados manualmente de una llamada al método InkEdit:: Recognize o automáticamente después de que se desencadene el tiempo de espera del reconocimiento.'
ms.assetid: 09618be0-fe49-494f-940f-79ff8352097e
title: Evento InkEdit. RecognitionResult (autodibujado. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d6206293b604e5540b5e6d0271e1ebe984a987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278859"
---
# <a name="inkeditrecognitionresult-event"></a><span data-ttu-id="0dc15-103">Evento InkEdit. RecognitionResult</span><span class="sxs-lookup"><span data-stu-id="0dc15-103">InkEdit.RecognitionResult event</span></span>

<span data-ttu-id="0dc15-104">Se produce cuando el control [InkEdit](inkedit-control-reference.md) obtiene los resultados manualmente de una llamada al método [**InkEdit:: Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) o automáticamente después de que se desencadene el tiempo de espera del reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="0dc15-104">Occurs when the [InkEdit](inkedit-control-reference.md) control gets results manually from a call to the [**InkEdit::Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) method or automatically after the recognition timeout fires.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dc15-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0dc15-105">Syntax</span></span>


```C++
void RecognitionResult(
  [in] IInkRecognitionResult *RecognitionResult
);
```



## <a name="parameters"></a><span data-ttu-id="0dc15-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0dc15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dc15-107">*RecognitionResult* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0dc15-107">*RecognitionResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc15-108">Un objeto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) que contiene el resultado del reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="0dc15-108">An [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object that contains the result of the recognition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dc15-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0dc15-109">Return value</span></span>

<span data-ttu-id="0dc15-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="0dc15-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dc15-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0dc15-111">Remarks</span></span>

<span data-ttu-id="0dc15-112">Este método de evento se define en la interfaz **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="0dc15-112">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="0dc15-113">La interfaz **\_ IInkEditEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IeeRecognitionResult.</span><span class="sxs-lookup"><span data-stu-id="0dc15-113">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeRecognitionResult.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dc15-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dc15-114">Requirements</span></span>



| <span data-ttu-id="0dc15-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dc15-115">Requirement</span></span> | <span data-ttu-id="0dc15-116">Value</span><span class="sxs-lookup"><span data-stu-id="0dc15-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dc15-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0dc15-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0dc15-118">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0dc15-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0dc15-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0dc15-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0dc15-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0dc15-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0dc15-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0dc15-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0dc15-122"><dt>Autodibujado. h (también requiere la intermano \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0dc15-122"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0dc15-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0dc15-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="0dc15-124"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0dc15-124"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0dc15-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0dc15-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dc15-126">InkEdit</span><span class="sxs-lookup"><span data-stu-id="0dc15-126">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

<span data-ttu-id="0dc15-127">[**Recognize Method \[ InkEdit control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)</span><span class="sxs-lookup"><span data-stu-id="0dc15-127">[**Recognize Method \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)</span></span>
</dt> </dl>

 

