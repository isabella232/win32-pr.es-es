---
description: El método SKIP omite el siguiente número de elementos especificado en la secuencia de enumeración.
ms.assetid: 825972c9-5303-4c5a-9475-dc67c185af91
title: 'IEnumMedia:: Skip (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd950fd61ad6f6b2030b03d0d269854f86e3a02d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681142"
---
# <a name="ienummediaskip-method"></a><span data-ttu-id="9a598-103">IEnumMedia:: Skip (método)</span><span class="sxs-lookup"><span data-stu-id="9a598-103">IEnumMedia::Skip method</span></span>

<span data-ttu-id="9a598-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9a598-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9a598-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="9a598-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9a598-106">El método **SKIP** omite el siguiente número de elementos especificado en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="9a598-106">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a598-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a598-107">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="9a598-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a598-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a598-109">*Celt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9a598-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a598-110">Número de elementos que se van a omitir.</span><span class="sxs-lookup"><span data-stu-id="9a598-110">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a598-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a598-111">Return value</span></span>

<span data-ttu-id="9a598-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="9a598-112">This method can return one of these values.</span></span>



| <span data-ttu-id="9a598-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9a598-113">Return code</span></span>                                                                             | <span data-ttu-id="9a598-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a598-114">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="9a598-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9a598-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="9a598-116">El número de elementos omitidos era *Celt*.</span><span class="sxs-lookup"><span data-stu-id="9a598-116">Number of elements skipped was *celt*.</span></span><br/>     |
| <dl> <span data-ttu-id="9a598-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="9a598-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="9a598-118">El número de elementos omitidos no era *Celt*.</span><span class="sxs-lookup"><span data-stu-id="9a598-118">Number of elements skipped was not *celt*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9a598-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a598-119">Requirements</span></span>



| <span data-ttu-id="9a598-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a598-120">Requirement</span></span> | <span data-ttu-id="9a598-121">Value</span><span class="sxs-lookup"><span data-stu-id="9a598-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a598-122">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="9a598-122">TAPI version</span></span><br/> | <span data-ttu-id="9a598-123">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="9a598-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9a598-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a598-124">Header</span></span><br/>       | <dl> <span data-ttu-id="9a598-125"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a598-125"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="9a598-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9a598-126">Library</span></span><br/>      | <dl> <span data-ttu-id="9a598-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a598-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9a598-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9a598-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="9a598-129"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a598-129"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a598-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a598-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a598-131">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="9a598-131">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




