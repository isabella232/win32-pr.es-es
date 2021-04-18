---
description: Se envía el mensaje DEVSPECIFICEX de línea de TAPI \_ para notificar a la aplicación los eventos específicos del dispositivo que se producen en una línea, una dirección o una llamada. El significado del mensaje y la interpretación de los parámetros son específicos del dispositivo.
ms.assetid: 137e91fd-a09e-430c-9d46-8e5be65f03d1
title: Mensaje de LINE_DEVSPECIFICEX (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba25047858c641ea4c6cec7d15ba06df24e8ee39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680626"
---
# <a name="line_devspecificex-message"></a><span data-ttu-id="de38f-104">Mensaje de línea \_ DEVSPECIFICEX</span><span class="sxs-lookup"><span data-stu-id="de38f-104">LINE\_DEVSPECIFICEX message</span></span>

<span data-ttu-id="de38f-105">Se envía el mensaje **\_ DEVSPECIFICEX de línea** de TAPI para notificar a la aplicación los eventos específicos del dispositivo que se producen en una línea, una dirección o una llamada.</span><span class="sxs-lookup"><span data-stu-id="de38f-105">The TAPI **LINE\_DEVSPECIFICEX** message is sent to notify the application about device-specific events occurring on a line, address, or call.</span></span> <span data-ttu-id="de38f-106">El significado del mensaje y la interpretación de los parámetros son específicos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="de38f-106">The meaning of the message and the interpretation of the parameters are device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="de38f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de38f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de38f-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="de38f-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="de38f-109">Identificador de un dispositivo de línea o de una llamada a.</span><span class="sxs-lookup"><span data-stu-id="de38f-109">A handle to either a line device or call.</span></span> <span data-ttu-id="de38f-110">Este parámetro es específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="de38f-110">This parameter is device specific.</span></span>

</dd> <dt>

<span data-ttu-id="de38f-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="de38f-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="de38f-112">Instancia de devolución de llamada proporcionada al abrir la línea.</span><span class="sxs-lookup"><span data-stu-id="de38f-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="de38f-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="de38f-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="de38f-114">Específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="de38f-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="de38f-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="de38f-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="de38f-116">Específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="de38f-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="de38f-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="de38f-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="de38f-118">Específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="de38f-118">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de38f-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de38f-119">Return value</span></span>

<span data-ttu-id="de38f-120">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="de38f-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de38f-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de38f-121">Remarks</span></span>

<span data-ttu-id="de38f-122">Un proveedor de servicios usa el mensaje **line \_ DEVSPECIFICEX** junto con la función [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) .</span><span class="sxs-lookup"><span data-stu-id="de38f-122">The **LINE\_DEVSPECIFICEX** message is used by a service provider in conjunction with the [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) function.</span></span> <span data-ttu-id="de38f-123">Su significado es específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="de38f-123">Its meaning is device specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="de38f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de38f-124">Requirements</span></span>



| <span data-ttu-id="de38f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="de38f-125">Requirement</span></span> | <span data-ttu-id="de38f-126">Value</span><span class="sxs-lookup"><span data-stu-id="de38f-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="de38f-127">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="de38f-127">TAPI version</span></span><br/> | <span data-ttu-id="de38f-128">Requiere TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="de38f-128">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="de38f-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de38f-129">Header</span></span><br/>       | <dl> <span data-ttu-id="de38f-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="de38f-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




