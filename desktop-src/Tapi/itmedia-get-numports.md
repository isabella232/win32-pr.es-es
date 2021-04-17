---
description: El \_ método get NumPorts obtiene el número de puertos necesarios para la sesión. La sesión utiliza el número especificado de puertos a partir del valor devuelto por Get \_ StartPort.
ms.assetid: 9ebdcf51-e095-4173-97d6-7754560abfb5
title: 'Método ITMedia:: get_NumPorts (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc223ddd5d210d2c1d440c52ca4201ccd6334b08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681218"
---
# <a name="itmediaget_numports-method"></a><span data-ttu-id="f1841-104">ITMedia:: get \_ NumPorts (método)</span><span class="sxs-lookup"><span data-stu-id="f1841-104">ITMedia::get\_NumPorts method</span></span>

<span data-ttu-id="f1841-105">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f1841-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f1841-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="f1841-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f1841-107">El método **Get \_ NumPorts** obtiene el número de puertos necesarios para la sesión.</span><span class="sxs-lookup"><span data-stu-id="f1841-107">The **get\_NumPorts** method gets the number of ports needed for the session.</span></span> <span data-ttu-id="f1841-108">La sesión utiliza el número especificado de puertos a partir del valor devuelto por [**Get \_ StartPort**](itmedia-get-startport.md).</span><span class="sxs-lookup"><span data-stu-id="f1841-108">The session uses the specified number of ports starting from the value returned by [**get\_StartPort**](itmedia-get-startport.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f1841-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1841-109">Syntax</span></span>


```C++
HRESULT get_NumPorts(
  [out] LONG *pNumPorts
);
```



## <a name="parameters"></a><span data-ttu-id="f1841-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1841-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1841-111">*pNumPorts* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f1841-111">*pNumPorts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1841-112">Puntero al número de puertos.</span><span class="sxs-lookup"><span data-stu-id="f1841-112">Pointer to the number of ports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1841-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1841-113">Return value</span></span>

<span data-ttu-id="f1841-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f1841-114">This method can return one of these values.</span></span>



| <span data-ttu-id="f1841-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f1841-115">Return code</span></span>                                                                                   | <span data-ttu-id="f1841-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1841-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f1841-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f1841-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f1841-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f1841-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f1841-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="f1841-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f1841-120">El parámetro *pNumPorts* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="f1841-120">The *pNumPorts* parameter is not a valid pointer.</span></span><br/>    |
| <dl> <span data-ttu-id="f1841-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f1841-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f1841-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="f1841-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="f1841-123"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="f1841-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="f1841-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="f1841-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="f1841-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="f1841-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="f1841-126">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="f1841-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="f1841-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1841-127">Requirements</span></span>



| <span data-ttu-id="f1841-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1841-128">Requirement</span></span> | <span data-ttu-id="f1841-129">Value</span><span class="sxs-lookup"><span data-stu-id="f1841-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1841-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="f1841-130">TAPI version</span></span><br/> | <span data-ttu-id="f1841-131">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="f1841-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f1841-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1841-132">Header</span></span><br/>       | <dl> <span data-ttu-id="f1841-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1841-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f1841-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1841-134">Library</span></span><br/>      | <dl> <span data-ttu-id="f1841-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1841-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f1841-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f1841-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="f1841-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1841-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1841-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1841-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1841-139">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="f1841-139">**ITMedia**</span></span>](itmedia.md)
</dt> </dl>

 

 




