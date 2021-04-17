---
description: El \_ mensaje de respuesta de línea TAPI se envía para informar de los resultados de las llamadas a funciones que se completaron de forma asincrónica.
ms.assetid: 5d98ed8b-b75e-49f8-aba3-c6eee89e91c1
title: Mensaje de LINE_REPLY (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed963a777a5073b0182e809eec83fb7f904768e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690977"
---
# <a name="line_reply-message"></a><span data-ttu-id="b529e-103">Mensaje de respuesta de línea \_</span><span class="sxs-lookup"><span data-stu-id="b529e-103">LINE\_REPLY message</span></span>

<span data-ttu-id="b529e-104">El mensaje **de \_ respuesta de línea** TAPI se envía para informar de los resultados de las llamadas a funciones que se completaron de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b529e-104">The TAPI **LINE\_REPLY** message is sent to report the results of function calls that completed asynchronously.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="b529e-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b529e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b529e-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="b529e-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="b529e-107">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b529e-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b529e-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="b529e-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="b529e-109">Devuelve la instancia de devolución de llamada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b529e-109">Returns the application's callback instance.</span></span>

</dd> <dt>

<span data-ttu-id="b529e-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="b529e-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="b529e-111">Identificador de solicitud para el que es la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b529e-111">The request identifier for which this is the reply.</span></span>

</dd> <dt>

<span data-ttu-id="b529e-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="b529e-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="b529e-113">La indicación de error o correcto.</span><span class="sxs-lookup"><span data-stu-id="b529e-113">The success or error indication.</span></span> <span data-ttu-id="b529e-114">La aplicación debe convertir este parámetro en un valor LONG.</span><span class="sxs-lookup"><span data-stu-id="b529e-114">The application should cast this parameter into a LONG.</span></span> <span data-ttu-id="b529e-115">Cero indica que se ha realizado correctamente; un número negativo indica un error.</span><span class="sxs-lookup"><span data-stu-id="b529e-115">Zero indicates success; a negative number indicates an error.</span></span>

</dd> <dt>

<span data-ttu-id="b529e-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="b529e-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="b529e-117">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="b529e-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b529e-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b529e-118">Return value</span></span>

<span data-ttu-id="b529e-119">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b529e-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b529e-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b529e-120">Remarks</span></span>

<span data-ttu-id="b529e-121">Las funciones que operan de forma asincrónica devuelven un valor de identificador de solicitud positivo a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b529e-121">Functions that operate asynchronously return a positive request identifier value to the application.</span></span> <span data-ttu-id="b529e-122">Este identificador de solicitud se devuelve con el mensaje de respuesta para identificar la solicitud que se completó.</span><span class="sxs-lookup"><span data-stu-id="b529e-122">This request identifier is returned with the reply message to identify the request that was completed.</span></span> <span data-ttu-id="b529e-123">El otro parámetro para el mensaje de **\_ respuesta de línea** contiene la indicación de éxito o error.</span><span class="sxs-lookup"><span data-stu-id="b529e-123">The other parameter for the **LINE\_REPLY** message carries the success or failure indication.</span></span> <span data-ttu-id="b529e-124">Los errores posibles son los mismos que los definidos por la función correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b529e-124">Possible errors are the same as those defined by the corresponding function.</span></span> <span data-ttu-id="b529e-125">Este mensaje no se puede deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="b529e-125">This message cannot be disabled.</span></span>

<span data-ttu-id="b529e-126">En algunos casos, es posible que una aplicación no reciba el mensaje de **\_ respuesta de línea** correspondiente a una llamada a una función asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b529e-126">In some cases, an application may fail to receive the **LINE\_REPLY** message corresponding to a call to an asynchronous function.</span></span> <span data-ttu-id="b529e-127">Esto sucede si se cancela la asignación del identificador de llamada correspondiente antes de que se haya recibido el mensaje.</span><span class="sxs-lookup"><span data-stu-id="b529e-127">This occurs if the corresponding call handle is deallocated before the message has been received.</span></span>

> [!Note]  
> <span data-ttu-id="b529e-128">Cuando una aplicación invoca cualquier operación asincrónica que vuelva a escribir datos en la memoria de la aplicación, la aplicación debe mantener esa memoria disponible para escritura hasta que se reciba un mensaje de línea o **\_ respuesta de línea** [**\_ GATHERDIGITS**](line-gatherdigits.md) .</span><span class="sxs-lookup"><span data-stu-id="b529e-128">When an application invokes any asynchronous operation that writes data back into application memory, the application must keep that memory available for writing until a **LINE\_REPLY** or [**LINE\_GATHERDIGITS**](line-gatherdigits.md) message is received.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b529e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b529e-129">Requirements</span></span>



| <span data-ttu-id="b529e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b529e-130">Requirement</span></span> | <span data-ttu-id="b529e-131">Value</span><span class="sxs-lookup"><span data-stu-id="b529e-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b529e-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="b529e-132">TAPI version</span></span><br/> | <span data-ttu-id="b529e-133">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="b529e-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b529e-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b529e-134">Header</span></span><br/>       | <dl> <span data-ttu-id="b529e-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b529e-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b529e-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="b529e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b529e-137">**LÍNEA \_ GATHERDIGITS**</span><span class="sxs-lookup"><span data-stu-id="b529e-137">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> </dl>

 

 




