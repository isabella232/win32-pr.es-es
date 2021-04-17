---
description: El \_ mensaje line QUEUESTATUS se envía cuando el estado de una cola de ACD cambia en un controlador de agente para el que la aplicación tiene actualmente una línea abierta. Este mensaje se genera mediante la función lineProxyMessage.
ms.assetid: 9baacfc5-f26c-41c7-a1f8-f48ec8aa844c
title: Mensaje de LINE_QUEUESTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a89785b92009a7531ae693545febaf153cf19bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690503"
---
# <a name="line_queuestatus-message"></a><span data-ttu-id="3320c-104">Mensaje de línea \_ QUEUESTATUS</span><span class="sxs-lookup"><span data-stu-id="3320c-104">LINE\_QUEUESTATUS message</span></span>

<span data-ttu-id="3320c-105">El mensaje **line \_ QUEUESTATUS** se envía cuando el estado de una cola de ACD cambia en un controlador de agente para el que la aplicación tiene actualmente una línea abierta.</span><span class="sxs-lookup"><span data-stu-id="3320c-105">The **LINE\_QUEUESTATUS** message is sent when the status of an ACD queue changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="3320c-106">Este mensaje se genera mediante la función [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .</span><span class="sxs-lookup"><span data-stu-id="3320c-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="3320c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3320c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3320c-108">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="3320c-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="3320c-109">Identificador de la aplicación para el dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="3320c-109">The application's handle to the line device.</span></span> <span data-ttu-id="3320c-110">Esto se relaciona con el controlador del agente.</span><span class="sxs-lookup"><span data-stu-id="3320c-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="3320c-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="3320c-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="3320c-112">Instancia de devolución de llamada proporcionada al abrir la línea.</span><span class="sxs-lookup"><span data-stu-id="3320c-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="3320c-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="3320c-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="3320c-114">El identificador de la cola cuyo estado ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="3320c-114">The identifier of the queue whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="3320c-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="3320c-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="3320c-116">Especifica el estado de la cola que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="3320c-116">Specifies the queue status that has changed.</span></span> <span data-ttu-id="3320c-117">Puede ser una o varias de las [**\_ constantes LINEQUEUESTATUS**](linequeuestatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="3320c-117">Can be one or more of the [**LINEQUEUESTATUS\_ constants**](linequeuestatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="3320c-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="3320c-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="3320c-119">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3320c-119">Reserved.</span></span> <span data-ttu-id="3320c-120">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="3320c-120">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3320c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3320c-121">Requirements</span></span>



| <span data-ttu-id="3320c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3320c-122">Requirement</span></span> | <span data-ttu-id="3320c-123">Value</span><span class="sxs-lookup"><span data-stu-id="3320c-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3320c-124">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="3320c-124">TAPI version</span></span><br/> | <span data-ttu-id="3320c-125">Requiere TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="3320c-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="3320c-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3320c-126">Header</span></span><br/>       | <dl> <span data-ttu-id="3320c-127"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="3320c-127"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3320c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3320c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3320c-129">**lineProxyMessage**</span><span class="sxs-lookup"><span data-stu-id="3320c-129">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




