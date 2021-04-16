---
description: Mensajes de calidad
ms.assetid: ff98cb51-6300-470d-b696-5e27591c6b3f
title: Mensajes de calidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b290833be7550e255590a5bcda449ce19743c0b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537149"
---
# <a name="quality-messages"></a><span data-ttu-id="7f4a9-103">Mensajes de calidad</span><span class="sxs-lookup"><span data-stu-id="7f4a9-103">Quality Messages</span></span>

<span data-ttu-id="7f4a9-104">Los mensajes de calidad se definen con la estructura de [**calidad**](/windows/win32/api/strmif/ns-strmif-quality) .</span><span class="sxs-lookup"><span data-stu-id="7f4a9-104">Quality messages are defined with the [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure.</span></span> <span data-ttu-id="7f4a9-105">Esta estructura contiene los siguientes miembros:</span><span class="sxs-lookup"><span data-stu-id="7f4a9-105">This structure contains the following members:</span></span>

-   <span data-ttu-id="7f4a9-106">**Tipo:** Definido por la enumeración [**QualityMessageType**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) ; Famine, que indica que el filtro está recibiendo demasiados datos, o inundaciones, que indican que el filtro está recibiendo demasiados datos.</span><span class="sxs-lookup"><span data-stu-id="7f4a9-106">**Type:** Defined by the [**QualityMessageType**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) enumeration; either Famine, indicating that the filter is receiving too little data, or Flood, indicating that the filter is receiving too much data.</span></span>
-   <span data-ttu-id="7f4a9-107">**Proporción:** Ajuste solicitado en la velocidad de datos, de una línea base de 1000.</span><span class="sxs-lookup"><span data-stu-id="7f4a9-107">**Proportion:** The requested adjustment in the data rate, from a baseline of 1000.</span></span> <span data-ttu-id="7f4a9-108">Por ejemplo, 750 indica 75% y 1500 indica 150%.</span><span class="sxs-lookup"><span data-stu-id="7f4a9-108">For example, 750 indicates 75% and 1500 indicates 150%.</span></span>
-   <span data-ttu-id="7f4a9-109">**Tardía:** Tiempo de referencia que indica en qué momento llegó la muestra más reciente.</span><span class="sxs-lookup"><span data-stu-id="7f4a9-109">**Late:** Reference time indicating how late the most recent sample arrived.</span></span> <span data-ttu-id="7f4a9-110">El valor es negativo si el ejemplo llegó pronto.</span><span class="sxs-lookup"><span data-stu-id="7f4a9-110">The value is negative if the sample arrived early.</span></span>
-   <span data-ttu-id="7f4a9-111">**Marca** de tiempo: Marca de tiempo de la muestra más reciente.</span><span class="sxs-lookup"><span data-stu-id="7f4a9-111">**TimeStamp:** The time stamp on the most recent sample.</span></span>

<span data-ttu-id="7f4a9-112">Por ejemplo, supongamos que un ejemplo con una marca de tiempo de 240 milisegundos (MS) alcanza el representador en 280 MS, tiempo de secuencia.</span><span class="sxs-lookup"><span data-stu-id="7f4a9-112">For example, suppose that a sample with a time stamp of 240 milliseconds (ms) reaches the renderer at 280 ms, stream time.</span></span> <span data-ttu-id="7f4a9-113">El representador crea un mensaje de calidad de tipo Famine.</span><span class="sxs-lookup"><span data-stu-id="7f4a9-113">The renderer creates a quality message of type Famine.</span></span> <span data-ttu-id="7f4a9-114">El ejemplo llegó a 40 ms en tiempo de espera, por lo que el **último** miembro es 400000.</span><span class="sxs-lookup"><span data-stu-id="7f4a9-114">The sample arrived 40 ms late, so the **Late** member is 400000.</span></span> <span data-ttu-id="7f4a9-115">(Todos los tiempos de referencia están en unidades de 100 a nanosegundos). El miembro **timestamp** es 2,4 millones.</span><span class="sxs-lookup"><span data-stu-id="7f4a9-115">(All reference times are in 100-nanosecond units.) The **TimeStamp** member is 2400000.</span></span>

<span data-ttu-id="7f4a9-116">En el caso del miembro **proporcional** , el representador podría usar un promedio de ejecución para calcular el valor.</span><span class="sxs-lookup"><span data-stu-id="7f4a9-116">For the **Proportion** member, the renderer might use a running average to calculate the value.</span></span> <span data-ttu-id="7f4a9-117">Es posible que las muestras hayan llegado a tiempo y este ejemplo sea una anomalía.</span><span class="sxs-lookup"><span data-stu-id="7f4a9-117">Perhaps samples have been arriving on time, and this sample is an anomaly.</span></span> <span data-ttu-id="7f4a9-118">En ese caso, es posible que el representador solicite solo una pequeña corrección.</span><span class="sxs-lookup"><span data-stu-id="7f4a9-118">In that case the renderer might request only a small correction.</span></span> <span data-ttu-id="7f4a9-119">Por otro lado, si las muestras se atrasan constantemente, el representador podría solicitar una corrección mayor.</span><span class="sxs-lookup"><span data-stu-id="7f4a9-119">On the other hand, if samples are consistently late, the renderer might request a larger correction.</span></span>

<span data-ttu-id="7f4a9-120">El control de calidad se controla a través de la interfaz [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) .</span><span class="sxs-lookup"><span data-stu-id="7f4a9-120">Quality control is handled through the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface.</span></span> <span data-ttu-id="7f4a9-121">Contiene dos métodos.</span><span class="sxs-lookup"><span data-stu-id="7f4a9-121">It contains two methods.</span></span>

-   <span data-ttu-id="7f4a9-122">[**Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify): envía un mensaje de calidad.</span><span class="sxs-lookup"><span data-stu-id="7f4a9-122">[**Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify): Sends a quality message.</span></span>
-   <span data-ttu-id="7f4a9-123">[**SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink): especifica un administrador de calidad personalizado.</span><span class="sxs-lookup"><span data-stu-id="7f4a9-123">[**SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink): Specifies a custom quality manager.</span></span>

<span data-ttu-id="7f4a9-124">Un objeto que implementa **IQualityControl** recibe mensajes de calidad a través de su método **Notify** .</span><span class="sxs-lookup"><span data-stu-id="7f4a9-124">An object that implements **IQualityControl** receives quality messages through its **Notify** method.</span></span> <span data-ttu-id="7f4a9-125">Puede controlar el mensaje o pasar el mensaje a otro objeto.</span><span class="sxs-lookup"><span data-stu-id="7f4a9-125">It can either handle the message or pass the message to another object.</span></span> <span data-ttu-id="7f4a9-126">Si la aplicación llama al método **SetSink** del objeto, el objeto debe delegar el control de calidad al administrador de calidad especificado.</span><span class="sxs-lookup"><span data-stu-id="7f4a9-126">If the application calls the object's **SetSink** method, the object should delegate quality control to the specified quality manager.</span></span>

 

 



