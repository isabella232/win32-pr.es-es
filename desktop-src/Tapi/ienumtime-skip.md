---
description: 'Método IEnumTime::Skip: el método Skip omite el siguiente número especificado de elementos en la secuencia de enumeración.'
ms.assetid: e4d9c95d-1b68-4af6-beb2-2014074e5089
title: Método IEnumTime::Skip (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 190a98c14cb8f551276a173e2d73872d876f2ceb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090723"
---
# <a name="ienumtimeskip-method"></a><span data-ttu-id="89eb3-103">IEnumTime::Skip (método)</span><span class="sxs-lookup"><span data-stu-id="89eb3-103">IEnumTime::Skip method</span></span>

<span data-ttu-id="89eb3-104">\[ Los controles e interfaces de conferencia de telefonía IP de Encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="89eb3-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="89eb3-105">La API de cliente RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="89eb3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="89eb3-106">El **método Skip** omite el siguiente número especificado de elementos en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="89eb3-106">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="89eb3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89eb3-107">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="89eb3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89eb3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89eb3-109">*celta* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="89eb3-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89eb3-110">Número de elementos que se van a omitir.</span><span class="sxs-lookup"><span data-stu-id="89eb3-110">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89eb3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89eb3-111">Return value</span></span>

<span data-ttu-id="89eb3-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="89eb3-112">This method can return one of these values.</span></span>



| <span data-ttu-id="89eb3-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="89eb3-113">Return code</span></span>                                                                             | <span data-ttu-id="89eb3-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="89eb3-114">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="89eb3-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="89eb3-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="89eb3-116">El número de elementos omitido fue *celt*.</span><span class="sxs-lookup"><span data-stu-id="89eb3-116">Number of elements skipped was *celt*.</span></span><br/>     |
| <dl> <span data-ttu-id="89eb3-117"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="89eb3-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="89eb3-118">El número de elementos omitido no era *de centígrados.*</span><span class="sxs-lookup"><span data-stu-id="89eb3-118">Number of elements skipped was not *celt*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="89eb3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89eb3-119">Requirements</span></span>



| <span data-ttu-id="89eb3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="89eb3-120">Requirement</span></span> | <span data-ttu-id="89eb3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="89eb3-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89eb3-122">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="89eb3-122">TAPI version</span></span><br/> | <span data-ttu-id="89eb3-123">Requiere TAPI 3.0 o posterior</span><span class="sxs-lookup"><span data-stu-id="89eb3-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="89eb3-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89eb3-124">Header</span></span><br/>       | <dl> <span data-ttu-id="89eb3-125"><dt>Sdpblb.h</dt></span><span class="sxs-lookup"><span data-stu-id="89eb3-125"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="89eb3-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="89eb3-126">Library</span></span><br/>      | <dl> <span data-ttu-id="89eb3-127"><dt>Uuid.lib</dt></span><span class="sxs-lookup"><span data-stu-id="89eb3-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="89eb3-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="89eb3-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="89eb3-129"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89eb3-129"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89eb3-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="89eb3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89eb3-131">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="89eb3-131">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




