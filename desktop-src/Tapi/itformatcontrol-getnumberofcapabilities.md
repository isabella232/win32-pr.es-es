---
description: El método GetNumberOfCapabilities recupera el número de funciones asociadas al formato actual.
ms.assetid: 26e51c0d-c1cb-410f-ab19-eb884afa8431
title: 'ITFormatControl:: GetNumberOfCapabilities (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29153f5ee9ce8c5e12b93a1d219905c40f80418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690536"
---
# <a name="itformatcontrolgetnumberofcapabilities-method"></a><span data-ttu-id="4d9e2-103">ITFormatControl:: GetNumberOfCapabilities (método)</span><span class="sxs-lookup"><span data-stu-id="4d9e2-103">ITFormatControl::GetNumberOfCapabilities method</span></span>

<span data-ttu-id="4d9e2-104">\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4d9e2-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4d9e2-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="4d9e2-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4d9e2-106">El método **GetNumberOfCapabilities** recupera el número de funciones asociadas al formato actual.</span><span class="sxs-lookup"><span data-stu-id="4d9e2-106">The **GetNumberOfCapabilities** method retrieves the number of capabilities associated with the current format.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d9e2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d9e2-107">Syntax</span></span>


```C++
HRESULT GetNumberOfCapabilities(
  [out] DWORD *pdwCount
);
```



## <a name="parameters"></a><span data-ttu-id="4d9e2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d9e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d9e2-109">*pdwCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4d9e2-109">*pdwCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d9e2-110">Recuento de las capacidades.</span><span class="sxs-lookup"><span data-stu-id="4d9e2-110">Count of the capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d9e2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d9e2-111">Return value</span></span>

<span data-ttu-id="4d9e2-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="4d9e2-112">This method can return one of these values.</span></span>



| <span data-ttu-id="4d9e2-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4d9e2-113">Return code</span></span>                                                                                   | <span data-ttu-id="4d9e2-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d9e2-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="4d9e2-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="4d9e2-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4d9e2-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="4d9e2-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4d9e2-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4d9e2-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4d9e2-118">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="4d9e2-118">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4d9e2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d9e2-119">Requirements</span></span>



| <span data-ttu-id="4d9e2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d9e2-120">Requirement</span></span> | <span data-ttu-id="4d9e2-121">Value</span><span class="sxs-lookup"><span data-stu-id="4d9e2-121">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4d9e2-122">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="4d9e2-122">TAPI version</span></span><br/> | <span data-ttu-id="4d9e2-123">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="4d9e2-123">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="4d9e2-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d9e2-124">Header</span></span><br/>       | <dl> <span data-ttu-id="4d9e2-125"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d9e2-125"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4d9e2-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4d9e2-126">Library</span></span><br/>      | <dl> <span data-ttu-id="4d9e2-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d9e2-127"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="4d9e2-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4d9e2-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="4d9e2-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d9e2-129"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d9e2-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d9e2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d9e2-131">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="4d9e2-131">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> </dl>

 

 




