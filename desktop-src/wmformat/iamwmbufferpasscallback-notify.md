---
title: Método NOTIFY de IAMWMBufferPassCallback
description: El PIN llama al método Notify para cada búfer que se entrega durante el streaming.
ms.assetid: 3f252754-c784-4ffd-bcfc-fab73fa02b9a
keywords:
- Método Notify formato de Windows Media
- Método Notify formato de Windows Media, interfaz IAMWMBufferPassCallback
- Interfaz IAMWMBufferPassCallback formato de Windows Media, método Notify
topic_type:
- apiref
api_name:
- IAMWMBufferPassCallback.Notify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8f362262b36dee0bfc9a18e57010d102b2fa2cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149525"
---
# <a name="iamwmbufferpasscallbacknotify-method"></a><span data-ttu-id="7b492-106">IAMWMBufferPassCallback:: NOTIFY (método)</span><span class="sxs-lookup"><span data-stu-id="7b492-106">IAMWMBufferPassCallback::Notify method</span></span>

<span data-ttu-id="7b492-107">El PIN llama al método **Notify** para cada búfer que se entrega durante el streaming.</span><span class="sxs-lookup"><span data-stu-id="7b492-107">The **Notify** method is called by the pin for each buffer that is delivered during streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b492-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b492-108">Syntax</span></span>


```C++
HRESULT Notify(
  [in] INSSBuffer3    *pNSSBuffer3,
  [in] IPin           *pPin,
  [in] REFERENCE_TIME *prtStart,
  [in] REFERENCE_TIME *prtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="7b492-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b492-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b492-110">*pNSSBuffer3* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7b492-110">*pNSSBuffer3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b492-111">Puntero a la interfaz [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) expuesta en el ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="7b492-111">Pointer to the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface exposed on the media sample.</span></span>

</dd> <dt>

<span data-ttu-id="7b492-112">*pPin* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7b492-112">*pPin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b492-113">Puntero al pin asociado a la secuencia de medios a la que pertenece el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="7b492-113">Pointer to the pin associated with the media stream that the sample belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="7b492-114">*prtStart* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7b492-114">*prtStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b492-115">Hora de inicio del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="7b492-115">Start time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="7b492-116">*prtEnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7b492-116">*prtEnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b492-117">Hora de finalización del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="7b492-117">End time of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b492-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b492-118">Return value</span></span>

<span data-ttu-id="7b492-119">No se especifica ningún valor devuelto determinado.</span><span class="sxs-lookup"><span data-stu-id="7b492-119">No particular return value is specified.</span></span> <span data-ttu-id="7b492-120">El PIN que realiza la llamada omite el **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7b492-120">The calling pin ignores the **HRESULT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b492-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b492-121">Remarks</span></span>

<span data-ttu-id="7b492-122">Este método permite que una aplicación examine y actúe sobre la información del búfer multimedia antes de que se procese el contenido del búfer.</span><span class="sxs-lookup"><span data-stu-id="7b492-122">This method enables an application to examine and act on information in the media buffer before the buffer contents are processed.</span></span> <span data-ttu-id="7b492-123">La aplicación es responsable de conocer el tipo de medio del PIN.</span><span class="sxs-lookup"><span data-stu-id="7b492-123">The application is responsible for knowing the media type on the pin.</span></span> <span data-ttu-id="7b492-124">Esta información se puede obtener obteniendo primero la información de la secuencia del perfil y, a continuación, llamando al método [**IConfigAsfWriter2:: StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) para determinar qué PIN está asociado a cada flujo.</span><span class="sxs-lookup"><span data-stu-id="7b492-124">This information can be obtained by first getting the stream information from the profile and then calling [**IConfigAsfWriter2::StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) method to determine which pin is associated with each stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b492-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b492-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b492-126">**Referencia de QASF de DirectShow**</span><span class="sxs-lookup"><span data-stu-id="7b492-126">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="7b492-127">**Interfaz IAMWMBufferPassCallback**</span><span class="sxs-lookup"><span data-stu-id="7b492-127">**IAMWMBufferPassCallback Interface**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)
</dt> <dt>

[<span data-ttu-id="7b492-128">**Interfaz INSSBuffer3**</span><span class="sxs-lookup"><span data-stu-id="7b492-128">**INSSBuffer3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
</dt> </dl>

 

 