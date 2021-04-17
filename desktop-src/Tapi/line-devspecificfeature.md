---
description: Se envía el mensaje DEVSPECIFICFEATURE de línea de TAPI \_ para notificar a la aplicación los eventos específicos del dispositivo que se producen en una línea, una dirección o una llamada. El significado del mensaje y la interpretación de los parámetros son específicos del dispositivo.
ms.assetid: 5f1a4da2-1a2a-4a18-8a69-82d27ddca9cf
title: Mensaje de LINE_DEVSPECIFICFEATURE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d45f91f4b3d45b52a345827e6535b054e9cf2c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691069"
---
# <a name="line_devspecificfeature-message"></a><span data-ttu-id="24ba6-104">Mensaje de línea \_ DEVSPECIFICFEATURE</span><span class="sxs-lookup"><span data-stu-id="24ba6-104">LINE\_DEVSPECIFICFEATURE message</span></span>

<span data-ttu-id="24ba6-105">Se envía el mensaje **\_ DEVSPECIFICFEATURE de línea** de TAPI para notificar a la aplicación los eventos específicos del dispositivo que se producen en una línea, una dirección o una llamada.</span><span class="sxs-lookup"><span data-stu-id="24ba6-105">The TAPI **LINE\_DEVSPECIFICFEATURE** message is sent to notify the application about device-specific events occurring on a line, address, or call.</span></span> <span data-ttu-id="24ba6-106">El significado del mensaje y la interpretación de los parámetros son específicos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="24ba6-106">The meaning of the message and the interpretation of the parameters are device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="24ba6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24ba6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24ba6-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="24ba6-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="24ba6-109">Identificador de un dispositivo de línea o de una llamada a.</span><span class="sxs-lookup"><span data-stu-id="24ba6-109">A handle to either a line device or call.</span></span> <span data-ttu-id="24ba6-110">Esto es específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="24ba6-110">This is device specific.</span></span>

</dd> <dt>

<span data-ttu-id="24ba6-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="24ba6-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="24ba6-112">Instancia de devolución de llamada proporcionada al abrir la línea.</span><span class="sxs-lookup"><span data-stu-id="24ba6-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="24ba6-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="24ba6-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="24ba6-114">Específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="24ba6-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="24ba6-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="24ba6-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="24ba6-116">Específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="24ba6-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="24ba6-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="24ba6-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="24ba6-118">Específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="24ba6-118">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24ba6-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24ba6-119">Return value</span></span>

<span data-ttu-id="24ba6-120">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="24ba6-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="24ba6-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="24ba6-121">Remarks</span></span>

<span data-ttu-id="24ba6-122">Un proveedor de servicios usa el mensaje **line \_ DEVSPECIFICFEATURE** junto con la función [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) .</span><span class="sxs-lookup"><span data-stu-id="24ba6-122">The **LINE\_DEVSPECIFICFEATURE** message is used by a service provider in conjunction with the [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) function.</span></span> <span data-ttu-id="24ba6-123">Su significado es específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="24ba6-123">Its meaning is device specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="24ba6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24ba6-124">Requirements</span></span>



| <span data-ttu-id="24ba6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="24ba6-125">Requirement</span></span> | <span data-ttu-id="24ba6-126">Value</span><span class="sxs-lookup"><span data-stu-id="24ba6-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="24ba6-127">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="24ba6-127">TAPI version</span></span><br/> | <span data-ttu-id="24ba6-128">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="24ba6-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="24ba6-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="24ba6-129">Header</span></span><br/>       | <dl> <span data-ttu-id="24ba6-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="24ba6-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




