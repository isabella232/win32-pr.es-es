---
description: El método SKIP omite el siguiente número de elementos especificado en la secuencia de enumeración.
ms.assetid: e4d9c95d-1b68-4af6-beb2-2014074e5089
title: 'IEnumTime:: Skip (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebd157afc51f52a8453c38f8a14702476c46eb9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690702"
---
# <a name="ienumtimeskip-method"></a><span data-ttu-id="89146-103">IEnumTime:: Skip (método)</span><span class="sxs-lookup"><span data-stu-id="89146-103">IEnumTime::Skip method</span></span>

<span data-ttu-id="89146-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="89146-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="89146-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="89146-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="89146-106">El método **SKIP** omite el siguiente número de elementos especificado en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="89146-106">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="89146-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89146-107">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="89146-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89146-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89146-109">*Celt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="89146-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89146-110">Número de elementos que se van a omitir.</span><span class="sxs-lookup"><span data-stu-id="89146-110">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89146-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89146-111">Return value</span></span>

<span data-ttu-id="89146-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="89146-112">This method can return one of these values.</span></span>



| <span data-ttu-id="89146-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="89146-113">Return code</span></span>                                                                             | <span data-ttu-id="89146-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="89146-114">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="89146-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="89146-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="89146-116">El número de elementos omitidos era *Celt*.</span><span class="sxs-lookup"><span data-stu-id="89146-116">Number of elements skipped was *celt*.</span></span><br/>     |
| <dl> <span data-ttu-id="89146-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="89146-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="89146-118">El número de elementos omitidos no era *Celt*.</span><span class="sxs-lookup"><span data-stu-id="89146-118">Number of elements skipped was not *celt*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="89146-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89146-119">Requirements</span></span>



| <span data-ttu-id="89146-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="89146-120">Requirement</span></span> | <span data-ttu-id="89146-121">Value</span><span class="sxs-lookup"><span data-stu-id="89146-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89146-122">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="89146-122">TAPI version</span></span><br/> | <span data-ttu-id="89146-123">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="89146-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="89146-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89146-124">Header</span></span><br/>       | <dl> <span data-ttu-id="89146-125"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="89146-125"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="89146-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="89146-126">Library</span></span><br/>      | <dl> <span data-ttu-id="89146-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89146-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="89146-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="89146-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="89146-129"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89146-129"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89146-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="89146-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89146-131">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="89146-131">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




