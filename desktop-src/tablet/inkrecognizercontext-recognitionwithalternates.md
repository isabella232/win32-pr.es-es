---
description: Se produce cuando la clase InkRecognizerContext ha generado resultados después de llamar al método de método BackgroundRecognizeWithAlternates.
ms.assetid: 5e86a4d5-c0a7-4283-81cc-ec3a26f74880
title: Evento InkRecognizerContext. RecognitionWithAlternates (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a7d35d8281305b0cb5f84114bb2f2fa0e718c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277785"
---
# <a name="inkrecognizercontextrecognitionwithalternates-event"></a><span data-ttu-id="82c52-103">Evento InkRecognizerContext. RecognitionWithAlternates</span><span class="sxs-lookup"><span data-stu-id="82c52-103">InkRecognizerContext.RecognitionWithAlternates event</span></span>

<span data-ttu-id="82c52-104">Se produce cuando la [**clase InkRecognizerContext**](inkrecognizercontext-class.md) ha generado resultados después de llamar al método de [**método BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) .</span><span class="sxs-lookup"><span data-stu-id="82c52-104">Occurs when the [**InkRecognizerContext Class**](inkrecognizercontext-class.md) has generated results after calling the [**BackgroundRecognizeWithAlternates Method**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="82c52-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82c52-105">Syntax</span></span>


```C++
void RecognitionWithAlternates(
  [in] IInkRecognitionResult *RecognitionResult,
  [in] VARIANT               CustomData,
  [in] InkRecognitionStatus  RecognitionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="82c52-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82c52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82c52-107">*RecognitionResult* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82c52-107">*RecognitionResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82c52-108">Resultado del reconocimiento del evento.</span><span class="sxs-lookup"><span data-stu-id="82c52-108">The recognition result from the event.</span></span>

</dd> <dt>

<span data-ttu-id="82c52-109">*CustomData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82c52-109">*CustomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82c52-110">Datos personalizados para el resultado del reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="82c52-110">The custom data for the recognition result.</span></span>

<span data-ttu-id="82c52-111">Para obtener más información sobre la estructura de variante, vea [usar la biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="82c52-111">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="82c52-112">*RecognitionStatus* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82c52-112">*RecognitionStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82c52-113">El estado de reconocimiento en el resultado de reconocimiento más reciente.</span><span class="sxs-lookup"><span data-stu-id="82c52-113">The recognition status as of the most recent recognition result.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82c52-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82c52-114">Return value</span></span>

<span data-ttu-id="82c52-115">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="82c52-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82c52-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82c52-116">Remarks</span></span>

<span data-ttu-id="82c52-117">El comportamiento de la interfaz de programación de aplicaciones (API) es imprevisible si se intenta obtener acceso al objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) original desde el controlador de eventos de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="82c52-117">The behavior of the application programming interface (API) is unpredictable if you try to gain access to the original [**InkRecognizerContext**](inkrecognizercontext-class.md) object from the recognition event handler.</span></span> <span data-ttu-id="82c52-118">No intente hacerlo.</span><span class="sxs-lookup"><span data-stu-id="82c52-118">Do not attempt to do this.</span></span> <span data-ttu-id="82c52-119">En su lugar, si necesita hacerlo, cree una marca y establézcala en el controlador de eventos de [**reconocimiento**](inkrecognizercontext-recognition.md) .</span><span class="sxs-lookup"><span data-stu-id="82c52-119">Instead, if you need to do this, create a flag and set it in the [**Recognition**](inkrecognizercontext-recognition.md) event handler.</span></span> <span data-ttu-id="82c52-120">Después, puede sondear esa marca para determinar cuándo se deben cambiar las propiedades de **InkRecognizerContext** fuera del controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="82c52-120">Then you can poll that flag to determine when to change the **InkRecognizerContext** properties outside of the event handler.</span></span>

<span data-ttu-id="82c52-121">Este método de evento se define en la \_ interfaz IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="82c52-121">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="82c52-122">La \_ interfaz IInkEvents implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IRERecognitionWithAlternates.</span><span class="sxs-lookup"><span data-stu-id="82c52-122">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IRERecognitionWithAlternates.</span></span>

## <a name="requirements"></a><span data-ttu-id="82c52-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82c52-123">Requirements</span></span>



| <span data-ttu-id="82c52-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="82c52-124">Requirement</span></span> | <span data-ttu-id="82c52-125">Value</span><span class="sxs-lookup"><span data-stu-id="82c52-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82c52-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82c52-126">Minimum supported client</span></span><br/> | <span data-ttu-id="82c52-127">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="82c52-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="82c52-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82c52-128">Minimum supported server</span></span><br/> | <span data-ttu-id="82c52-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="82c52-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="82c52-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82c52-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="82c52-131"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="82c52-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="82c52-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="82c52-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="82c52-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82c52-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="82c52-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="82c52-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82c52-135">**Clase InkRecognizerContext**</span><span class="sxs-lookup"><span data-stu-id="82c52-135">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> <dt>

[<span data-ttu-id="82c52-136">**Método BackgroundRecognizeWithAlternates**</span><span class="sxs-lookup"><span data-stu-id="82c52-136">**BackgroundRecognizeWithAlternates Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)
</dt> <dt>

[<span data-ttu-id="82c52-137">**Recognize (método)**</span><span class="sxs-lookup"><span data-stu-id="82c52-137">**Recognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[<span data-ttu-id="82c52-138">**Interfaz IInkRecognitionResult**</span><span class="sxs-lookup"><span data-stu-id="82c52-138">**IInkRecognitionResult Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

