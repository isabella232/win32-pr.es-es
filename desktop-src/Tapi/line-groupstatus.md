---
description: El \_ mensaje line GROUPSTATUS se envía cuando cambia el estado de un grupo ACD en un controlador de agente para el que la aplicación tiene actualmente una línea abierta. Este mensaje se genera mediante la función lineProxyMessage.
ms.assetid: 1f3210fe-a7c8-4cfa-8e36-3a88e93d68bb
title: Mensaje de LINE_GROUPSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22fec7c4701ee7140c02cede1901ef7998e5b60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679467"
---
# <a name="line_groupstatus-message"></a><span data-ttu-id="c61c3-104">Mensaje de línea \_ GROUPSTATUS</span><span class="sxs-lookup"><span data-stu-id="c61c3-104">LINE\_GROUPSTATUS message</span></span>

<span data-ttu-id="c61c3-105">El mensaje **line \_ GROUPSTATUS** se envía cuando cambia el estado de un grupo ACD en un controlador de agente para el que la aplicación tiene actualmente una línea abierta.</span><span class="sxs-lookup"><span data-stu-id="c61c3-105">The **LINE\_GROUPSTATUS** message is sent when the status of an ACD group changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="c61c3-106">Este mensaje se genera mediante la función [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .</span><span class="sxs-lookup"><span data-stu-id="c61c3-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="c61c3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c61c3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c61c3-108">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="c61c3-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="c61c3-109">Identificador de la aplicación para el dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="c61c3-109">The application's handle to the line device.</span></span> <span data-ttu-id="c61c3-110">Esto se relaciona con el controlador del agente.</span><span class="sxs-lookup"><span data-stu-id="c61c3-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="c61c3-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="c61c3-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="c61c3-112">Instancia de devolución de llamada proporcionada al abrir la línea.</span><span class="sxs-lookup"><span data-stu-id="c61c3-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="c61c3-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="c61c3-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="c61c3-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c61c3-114">Reserved.</span></span> <span data-ttu-id="c61c3-115">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="c61c3-115">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="c61c3-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="c61c3-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="c61c3-117">Especifica el estado del grupo que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="c61c3-117">Specifies the group status that has changed.</span></span> <span data-ttu-id="c61c3-118">La aplicación puede invocar [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) para determinar los cambios en los grupos disponibles.</span><span class="sxs-lookup"><span data-stu-id="c61c3-118">The application can invoke [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) to determine the changes in available groups.</span></span> <span data-ttu-id="c61c3-119">El parámetro *dwParam2* es una o varias de las [**\_ constantes LINEGROUPSTATUS**](linegroupstatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="c61c3-119">The *dwParam2* parameter is one or more of the [**LINEGROUPSTATUS\_ constants**](linegroupstatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c61c3-120">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="c61c3-120">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="c61c3-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c61c3-121">Reserved.</span></span> <span data-ttu-id="c61c3-122">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="c61c3-122">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c61c3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c61c3-123">Requirements</span></span>



| <span data-ttu-id="c61c3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c61c3-124">Requirement</span></span> | <span data-ttu-id="c61c3-125">Value</span><span class="sxs-lookup"><span data-stu-id="c61c3-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c61c3-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="c61c3-126">TAPI version</span></span><br/> | <span data-ttu-id="c61c3-127">Requiere TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="c61c3-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="c61c3-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c61c3-128">Header</span></span><br/>       | <dl> <span data-ttu-id="c61c3-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c61c3-129"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c61c3-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c61c3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c61c3-131">**lineGetGroupList**</span><span class="sxs-lookup"><span data-stu-id="c61c3-131">**lineGetGroupList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista)
</dt> </dl>

 

 




