---
description: El método get obtiene el valor de una propiedad de control de calidad de llamada determinada.
ms.assetid: 0fec408e-2751-4c99-afe1-4337d22eff83
title: 'ITCallQualityControl:: get (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ea42768c173c0c073abe356e1ae6816a486a03c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680958"
---
# <a name="itcallqualitycontrolget-method"></a><span data-ttu-id="9c1b9-103">ITCallQualityControl:: get (método)</span><span class="sxs-lookup"><span data-stu-id="9c1b9-103">ITCallQualityControl::Get method</span></span>

<span data-ttu-id="9c1b9-104">\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9c1b9-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9c1b9-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="9c1b9-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9c1b9-106">El método **Get** obtiene el valor de una [propiedad de control de calidad de llamada](callqualityproperty.md)determinada.</span><span class="sxs-lookup"><span data-stu-id="9c1b9-106">The **Get** method gets the value of a given [call quality control property](callqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9c1b9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c1b9-107">Syntax</span></span>


```C++
HRESULT Get(
  [in]  CallQualityProperty Property,
  [out] long                *plValue,
  [out] TAPIControlFlags    *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="9c1b9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c1b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c1b9-109">*Propiedad* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9c1b9-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c1b9-110">Miembro de la enumeración [**CallQualityProperty**](callqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="9c1b9-110">Member of the [**CallQualityProperty**](callqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="9c1b9-111">*plValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9c1b9-111">*plValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c1b9-112">Valor de la *propiedad* de entrada.</span><span class="sxs-lookup"><span data-stu-id="9c1b9-112">Value of the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="9c1b9-113">*plFlags* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9c1b9-113">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c1b9-114">Valor de la enumeración [**TAPIControlFlags**](tapicontrolflags.md) que indica cómo se controla el valor de la *propiedad* .</span><span class="sxs-lookup"><span data-stu-id="9c1b9-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c1b9-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c1b9-115">Return value</span></span>

<span data-ttu-id="9c1b9-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="9c1b9-116">This method can return one of these values.</span></span>



| <span data-ttu-id="9c1b9-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9c1b9-117">Return code</span></span>                                                                                   | <span data-ttu-id="9c1b9-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c1b9-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="9c1b9-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9c1b9-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9c1b9-120">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="9c1b9-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9c1b9-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9c1b9-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9c1b9-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="9c1b9-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9c1b9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c1b9-123">Requirements</span></span>



| <span data-ttu-id="9c1b9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c1b9-124">Requirement</span></span> | <span data-ttu-id="9c1b9-125">Value</span><span class="sxs-lookup"><span data-stu-id="9c1b9-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9c1b9-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="9c1b9-126">TAPI version</span></span><br/> | <span data-ttu-id="9c1b9-127">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="9c1b9-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="9c1b9-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c1b9-128">Header</span></span><br/>       | <dl> <span data-ttu-id="9c1b9-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c1b9-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9c1b9-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c1b9-130">Library</span></span><br/>      | <dl> <span data-ttu-id="9c1b9-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c1b9-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="9c1b9-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9c1b9-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="9c1b9-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c1b9-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c1b9-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c1b9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c1b9-135">**ITCallQualityControl**</span><span class="sxs-lookup"><span data-stu-id="9c1b9-135">**ITCallQualityControl**</span></span>](itcallqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="9c1b9-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="9c1b9-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="9c1b9-137">**CallQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="9c1b9-137">**CallQualityProperty**</span></span>](callqualityproperty.md)
</dt> </dl>

 

 




