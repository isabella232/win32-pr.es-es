---
description: El \_ mensaje de respuesta del teléfono TAPI se envía a una aplicación para informar de los resultados de la llamada a función que se completó de forma asincrónica.
ms.assetid: 434f37d6-f385-4cc9-9658-2b683cab532c
title: Mensaje de PHONE_REPLY (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091920c631bf56d58959d60288a1af039495d2d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689943"
---
# <a name="phone_reply-message"></a><span data-ttu-id="786c9-103">Mensaje de respuesta de teléfono \_</span><span class="sxs-lookup"><span data-stu-id="786c9-103">PHONE\_REPLY message</span></span>

<span data-ttu-id="786c9-104">El mensaje **de \_ respuesta del teléfono** TAPI se envía a una aplicación para informar de los resultados de la llamada a función que se completó de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="786c9-104">The TAPI **PHONE\_REPLY** message is sent to an application to report the results of function call that completed asynchronously.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="786c9-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="786c9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="786c9-106">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="786c9-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="786c9-107">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="786c9-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="786c9-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="786c9-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="786c9-109">Devuelve la instancia de devolución de llamada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="786c9-109">Returns the application's callback instance.</span></span>

</dd> <dt>

<span data-ttu-id="786c9-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="786c9-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="786c9-111">Identificador de solicitud para el que es la respuesta.</span><span class="sxs-lookup"><span data-stu-id="786c9-111">The request identifier for which this is the reply.</span></span>

</dd> <dt>

<span data-ttu-id="786c9-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="786c9-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="786c9-113">La indicación de error o correcto.</span><span class="sxs-lookup"><span data-stu-id="786c9-113">The success or error indication.</span></span> <span data-ttu-id="786c9-114">La aplicación debe convertir este parámetro en un valor LONG.</span><span class="sxs-lookup"><span data-stu-id="786c9-114">The application should cast this parameter into a LONG.</span></span> <span data-ttu-id="786c9-115">Cero indica que se ha realizado correctamente; un número negativo indica un error.</span><span class="sxs-lookup"><span data-stu-id="786c9-115">Zero indicates success; a negative number indicates an error.</span></span>

</dd> <dt>

<span data-ttu-id="786c9-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="786c9-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="786c9-117">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="786c9-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="786c9-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="786c9-118">Return value</span></span>

<span data-ttu-id="786c9-119">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="786c9-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="786c9-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="786c9-120">Remarks</span></span>

<span data-ttu-id="786c9-121">Las funciones que operan de forma asincrónica devuelven un valor de identificador de solicitud positivo a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="786c9-121">Functions that operate asynchronously return a positive request identifier value to the application.</span></span> <span data-ttu-id="786c9-122">Este identificador de solicitud se devuelve con el mensaje de respuesta para identificar la solicitud que se completó.</span><span class="sxs-lookup"><span data-stu-id="786c9-122">This request identifier is returned with the reply message to identify the request that was completed.</span></span> <span data-ttu-id="786c9-123">El otro parámetro del mensaje **de \_ respuesta del teléfono** contiene la indicación de éxito o error.</span><span class="sxs-lookup"><span data-stu-id="786c9-123">The other parameter for the **PHONE\_REPLY** message carries the success or failure indication.</span></span> <span data-ttu-id="786c9-124">Los errores posibles son los mismos que los definidos por la función correspondiente.</span><span class="sxs-lookup"><span data-stu-id="786c9-124">Possible errors are the same as those defined by the corresponding function.</span></span> <span data-ttu-id="786c9-125">Este mensaje no se puede deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="786c9-125">This message cannot be disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="786c9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="786c9-126">Requirements</span></span>



| <span data-ttu-id="786c9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="786c9-127">Requirement</span></span> | <span data-ttu-id="786c9-128">Value</span><span class="sxs-lookup"><span data-stu-id="786c9-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="786c9-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="786c9-129">TAPI version</span></span><br/> | <span data-ttu-id="786c9-130">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="786c9-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="786c9-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="786c9-131">Header</span></span><br/>       | <dl> <span data-ttu-id="786c9-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="786c9-132"><dt>Tapi.h</dt></span></span> </dl> |



 

 




