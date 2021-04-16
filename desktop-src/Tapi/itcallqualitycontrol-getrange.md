---
description: El método GetRange obtiene el intervalo de valores válidos para una propiedad de calidad de llamada determinada.
ms.assetid: 974033cf-59ce-4593-93d7-290094c20a7c
title: 'ITCallQualityControl:: GetRange (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd3941ee8d7d0605cc6fefc61963065e4e5ba57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690404"
---
# <a name="itcallqualitycontrolgetrange-method"></a><span data-ttu-id="79651-103">ITCallQualityControl:: GetRange (método)</span><span class="sxs-lookup"><span data-stu-id="79651-103">ITCallQualityControl::GetRange method</span></span>

<span data-ttu-id="79651-104">\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="79651-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="79651-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="79651-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="79651-106">El método **GetRange** obtiene el intervalo de valores válidos para una [propiedad de calidad de llamada](callqualityproperty.md)determinada.</span><span class="sxs-lookup"><span data-stu-id="79651-106">The **GetRange** method gets the range of valid values for a given [call quality property](callqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="79651-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79651-107">Syntax</span></span>


```C++
HRESULT GetRange(
  [in]  CallQualityProperty Property,
  [out] long                *plMin,
  [out] long                *plMax,
  [out] long                *plSteppingDelta,
  [out] long                *plDefault,
  [out] TAPIControlFlags    *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="79651-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79651-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79651-109">*Propiedad* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79651-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79651-110">Miembro de la enumeración [**CallQualityProperty**](callqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="79651-110">Member of the [**CallQualityProperty**](callqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="79651-111">*plMin* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="79651-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79651-112">Valor mínimo válido para la propiedad de entrada.</span><span class="sxs-lookup"><span data-stu-id="79651-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="79651-113">*plMax* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="79651-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79651-114">Valor máximo válido para la propiedad de entrada.</span><span class="sxs-lookup"><span data-stu-id="79651-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="79651-115">*plSteppingDelta* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="79651-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79651-116">Incremento por el que se puede aumentar o disminuir el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="79651-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="79651-117">*plDefault* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="79651-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79651-118">Valor predeterminado del parámetro *Property* .</span><span class="sxs-lookup"><span data-stu-id="79651-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="79651-119">*plFlags* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="79651-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79651-120">Valor de la enumeración [**TAPIControlFlags**](tapicontrolflags.md) que indica cómo se controla el valor de la *propiedad* .</span><span class="sxs-lookup"><span data-stu-id="79651-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79651-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79651-121">Return value</span></span>

<span data-ttu-id="79651-122">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="79651-122">This method can return one of these values.</span></span>



| <span data-ttu-id="79651-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="79651-123">Return code</span></span>                                                                                   | <span data-ttu-id="79651-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="79651-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="79651-125"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="79651-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="79651-126">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="79651-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="79651-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="79651-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="79651-128">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="79651-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="79651-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79651-129">Requirements</span></span>



| <span data-ttu-id="79651-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="79651-130">Requirement</span></span> | <span data-ttu-id="79651-131">Value</span><span class="sxs-lookup"><span data-stu-id="79651-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="79651-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="79651-132">TAPI version</span></span><br/> | <span data-ttu-id="79651-133">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="79651-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="79651-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79651-134">Header</span></span><br/>       | <dl> <span data-ttu-id="79651-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="79651-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="79651-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79651-136">Library</span></span><br/>      | <dl> <span data-ttu-id="79651-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79651-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="79651-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79651-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="79651-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79651-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79651-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="79651-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79651-141">**ITCallQualityControl**</span><span class="sxs-lookup"><span data-stu-id="79651-141">**ITCallQualityControl**</span></span>](itcallqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="79651-142">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="79651-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="79651-143">**CallQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="79651-143">**CallQualityProperty**</span></span>](callqualityproperty.md)
</dt> </dl>

 

 




