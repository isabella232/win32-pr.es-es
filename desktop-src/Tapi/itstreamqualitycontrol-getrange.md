---
description: El método GetRange obtiene el intervalo de valores válidos para una propiedad de calidad de flujo determinada.
ms.assetid: 8c5e4652-1a40-4d7d-aa89-606e979dc03d
title: 'ITStreamQualityControl:: GetRange (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea8b20c2617eb0fe54ccc4603997464fca25f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690473"
---
# <a name="itstreamqualitycontrolgetrange-method"></a><span data-ttu-id="acc9f-103">ITStreamQualityControl:: GetRange (método)</span><span class="sxs-lookup"><span data-stu-id="acc9f-103">ITStreamQualityControl::GetRange method</span></span>

<span data-ttu-id="acc9f-104">\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="acc9f-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="acc9f-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="acc9f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="acc9f-106">El método **GetRange** obtiene el intervalo de valores válidos para una [**propiedad de calidad de flujo**](streamqualityproperty.md)determinada.</span><span class="sxs-lookup"><span data-stu-id="acc9f-106">The **GetRange** method gets the range of valid values for a given [**stream quality property**](streamqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="acc9f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="acc9f-107">Syntax</span></span>


```C++
HRESULT GetRange(
  [in]  StreamQualityProperty Property,
  [out] long                  *plMin,
  [out] long                  *plMax,
  [out] long                  *plSteppingDelta,
  [out] long                  *plDefault,
  [out] TAPIControlFlags      *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="acc9f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="acc9f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acc9f-109">*Propiedad* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="acc9f-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acc9f-110">Miembro de la enumeración [**StreamQualityProperty**](streamqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="acc9f-110">Member of the [**StreamQualityProperty**](streamqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="acc9f-111">*plMin* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="acc9f-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acc9f-112">Valor mínimo válido para la propiedad de entrada.</span><span class="sxs-lookup"><span data-stu-id="acc9f-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="acc9f-113">*plMax* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="acc9f-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acc9f-114">Valor máximo válido para la propiedad de entrada.</span><span class="sxs-lookup"><span data-stu-id="acc9f-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="acc9f-115">*plSteppingDelta* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="acc9f-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acc9f-116">Incremento por el que se puede aumentar o disminuir el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="acc9f-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="acc9f-117">*plDefault* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="acc9f-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acc9f-118">Valor predeterminado del parámetro *Property* .</span><span class="sxs-lookup"><span data-stu-id="acc9f-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="acc9f-119">*plFlags* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="acc9f-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acc9f-120">Valor de la enumeración [**TAPIControlFlags**](tapicontrolflags.md) que indica cómo se controla el valor de la *propiedad* .</span><span class="sxs-lookup"><span data-stu-id="acc9f-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acc9f-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="acc9f-121">Return value</span></span>

<span data-ttu-id="acc9f-122">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="acc9f-122">This method can return one of these values.</span></span>



| <span data-ttu-id="acc9f-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="acc9f-123">Return code</span></span>                                                                                   | <span data-ttu-id="acc9f-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="acc9f-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="acc9f-125"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="acc9f-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="acc9f-126">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="acc9f-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="acc9f-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="acc9f-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="acc9f-128">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="acc9f-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="acc9f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acc9f-129">Requirements</span></span>



| <span data-ttu-id="acc9f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="acc9f-130">Requirement</span></span> | <span data-ttu-id="acc9f-131">Value</span><span class="sxs-lookup"><span data-stu-id="acc9f-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="acc9f-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="acc9f-132">TAPI version</span></span><br/> | <span data-ttu-id="acc9f-133">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="acc9f-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="acc9f-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="acc9f-134">Header</span></span><br/>       | <dl> <span data-ttu-id="acc9f-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="acc9f-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="acc9f-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="acc9f-136">Library</span></span><br/>      | <dl> <span data-ttu-id="acc9f-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="acc9f-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="acc9f-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="acc9f-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="acc9f-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acc9f-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acc9f-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="acc9f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acc9f-141">**ITStreamQualityControl**</span><span class="sxs-lookup"><span data-stu-id="acc9f-141">**ITStreamQualityControl**</span></span>](itstreamqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="acc9f-142">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="acc9f-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="acc9f-143">**StreamQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="acc9f-143">**StreamQualityProperty**</span></span>](streamqualityproperty.md)
</dt> </dl>

 

 




