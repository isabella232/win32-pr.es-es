---
description: Se produce cuando InkRecognizerContext ha generado resultados del método BackgroundRecognize.
ms.assetid: 0cc319af-cd0b-4089-928b-cae6c86f6f61
title: Evento InkRecognizerContext. Recognition (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86da1a7470169f9f978e92a87f3e32f7e63acb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720680"
---
# <a name="inkrecognizercontextrecognition-event"></a><span data-ttu-id="5261a-103">Evento InkRecognizerContext. Recognition</span><span class="sxs-lookup"><span data-stu-id="5261a-103">InkRecognizerContext.Recognition event</span></span>

<span data-ttu-id="5261a-104">Se produce cuando [**InkRecognizerContext**](inkrecognizercontext-class.md) ha generado resultados del método [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) .</span><span class="sxs-lookup"><span data-stu-id="5261a-104">Occurs when the [**InkRecognizerContext**](inkrecognizercontext-class.md) has generated results from the [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5261a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5261a-105">Syntax</span></span>


```C++
void Recognition(
  [in] BSTR                 RecognizedString,
  [in] VARIANT              CustomData,
  [in] InkRecognitionStatus RecognitionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="5261a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5261a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5261a-107">*RecognizedString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5261a-107">*RecognizedString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5261a-108">El texto del resultado del reconocimiento con la mayor confianza.</span><span class="sxs-lookup"><span data-stu-id="5261a-108">The recognition result text with the highest confidence.</span></span>

<span data-ttu-id="5261a-109">Para obtener más información sobre el tipo de datos BSTR, vea el [uso de la biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="5261a-109">For more information about the BSTR data type, see the [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="5261a-110">*CustomData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5261a-110">*CustomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5261a-111">Objeto que contiene los datos personalizados para el resultado del reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="5261a-111">The object that contains the custom data for the recognition result.</span></span>

<span data-ttu-id="5261a-112">Para obtener más información acerca de la estructura de variante, vea el [uso de la biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="5261a-112">For more information about the VARIANT structure, see the [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="5261a-113">*RecognitionStatus* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5261a-113">*RecognitionStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5261a-114">El estado de reconocimiento en el resultado de reconocimiento más reciente.</span><span class="sxs-lookup"><span data-stu-id="5261a-114">The recognition status as of the most recent recognition result.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5261a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5261a-115">Return value</span></span>

<span data-ttu-id="5261a-116">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="5261a-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5261a-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5261a-117">Remarks</span></span>

<span data-ttu-id="5261a-118">El comportamiento de la interfaz de programación de aplicaciones (API) es imprevisible si se intenta obtener acceso al objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) original desde el controlador de eventos de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="5261a-118">The behavior of the application programming interface (API) is unpredictable if you try to gain access to the original [**InkRecognizerContext**](inkrecognizercontext-class.md) object from the recognition event handler.</span></span> <span data-ttu-id="5261a-119">No intente hacerlo.</span><span class="sxs-lookup"><span data-stu-id="5261a-119">Do not attempt to do this.</span></span> <span data-ttu-id="5261a-120">En su lugar, si necesita hacerlo, cree una marca y establézcala en el controlador de eventos de [reconocimiento](ink-recognition.md) .</span><span class="sxs-lookup"><span data-stu-id="5261a-120">Instead, if you need to do this, create a flag and set it in the [Recognition](ink-recognition.md) event handler.</span></span> <span data-ttu-id="5261a-121">Después, puede sondear esa marca para determinar cuándo se deben cambiar las propiedades de **InkRecognizerContext** fuera del controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="5261a-121">Then you can poll that flag to determine when to change the **InkRecognizerContext** properties outside of the event handler.</span></span>

<span data-ttu-id="5261a-122">Este método de evento se define en la \_ interfaz IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="5261a-122">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="5261a-123">La \_ interfaz IInkEvents implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IRERecognition.</span><span class="sxs-lookup"><span data-stu-id="5261a-123">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IRERecognition.</span></span>

## <a name="requirements"></a><span data-ttu-id="5261a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5261a-124">Requirements</span></span>



| <span data-ttu-id="5261a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5261a-125">Requirement</span></span> | <span data-ttu-id="5261a-126">Value</span><span class="sxs-lookup"><span data-stu-id="5261a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5261a-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5261a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5261a-128">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5261a-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5261a-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5261a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5261a-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5261a-130">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="5261a-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5261a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5261a-132"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5261a-132"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5261a-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5261a-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="5261a-134"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5261a-134"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="5261a-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="5261a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5261a-136">**Clase InkRecognizerContext**</span><span class="sxs-lookup"><span data-stu-id="5261a-136">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> <dt>

[<span data-ttu-id="5261a-137">**Método BackgroundRecognize**</span><span class="sxs-lookup"><span data-stu-id="5261a-137">**BackgroundRecognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)
</dt> <dt>

[<span data-ttu-id="5261a-138">**Enumeración InkRecognitionStatus**</span><span class="sxs-lookup"><span data-stu-id="5261a-138">**InkRecognitionStatus Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionstatus)
</dt> <dt>

[<span data-ttu-id="5261a-139">**Recognize (método)**</span><span class="sxs-lookup"><span data-stu-id="5261a-139">**Recognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[<span data-ttu-id="5261a-140">**Interfaz IInkRecognitionResult**</span><span class="sxs-lookup"><span data-stu-id="5261a-140">**IInkRecognitionResult Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

