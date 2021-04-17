---
description: El método GetRange recupera el intervalo de valores válidos para una propiedad de configuración de audio determinada.
ms.assetid: 09ee0c59-6ae6-47eb-a8cf-6b24e759d7fb
title: 'ITAudioSettings:: GetRange (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91dd4d7bed3134c17de9c5958c7e6184cd51918e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690092"
---
# <a name="itaudiosettingsgetrange-method"></a><span data-ttu-id="0ed59-103">ITAudioSettings:: GetRange (método)</span><span class="sxs-lookup"><span data-stu-id="0ed59-103">ITAudioSettings::GetRange method</span></span>

<span data-ttu-id="0ed59-104">\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0ed59-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0ed59-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="0ed59-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0ed59-106">El método **GetRange** recupera el intervalo de valores válidos para una [**propiedad de configuración de audio**](audiosettingsproperty.md)determinada.</span><span class="sxs-lookup"><span data-stu-id="0ed59-106">The **GetRange** method retrieves the range of valid values for a given [**audio settings property**](audiosettingsproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0ed59-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ed59-107">Syntax</span></span>


```C++
HRESULT get_Terminal(
  [out] ITTerminal **ppTerminal
);
```



## <a name="parameters"></a><span data-ttu-id="0ed59-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ed59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ed59-109">*Propiedad* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0ed59-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ed59-110">Miembro de la enumeración [**AudioSettingsProperty**](audiosettingsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="0ed59-110">Member of the [**AudioSettingsProperty**](audiosettingsproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="0ed59-111">*plMin* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0ed59-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ed59-112">Valor mínimo válido para la propiedad de entrada.</span><span class="sxs-lookup"><span data-stu-id="0ed59-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="0ed59-113">*plMax* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0ed59-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ed59-114">Valor máximo válido para la propiedad de entrada.</span><span class="sxs-lookup"><span data-stu-id="0ed59-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="0ed59-115">*plSteppingDelta* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0ed59-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ed59-116">Incremento por el que se puede aumentar o disminuir el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="0ed59-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="0ed59-117">*plDefault* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0ed59-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ed59-118">Valor predeterminado del parámetro *Property* .</span><span class="sxs-lookup"><span data-stu-id="0ed59-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ed59-119">*plFlags* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0ed59-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ed59-120">Valor de la enumeración [**TAPIControlFlags**](tapicontrolflags.md) que indica cómo se controla el valor de la *propiedad* .</span><span class="sxs-lookup"><span data-stu-id="0ed59-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ed59-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ed59-121">Return value</span></span>

<span data-ttu-id="0ed59-122">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0ed59-122">This method can return one of these values.</span></span>



| <span data-ttu-id="0ed59-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0ed59-123">Return code</span></span>                                                                                   | <span data-ttu-id="0ed59-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ed59-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0ed59-125"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0ed59-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0ed59-126">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0ed59-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0ed59-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0ed59-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0ed59-128">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="0ed59-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0ed59-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ed59-129">Requirements</span></span>



| <span data-ttu-id="0ed59-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ed59-130">Requirement</span></span> | <span data-ttu-id="0ed59-131">Value</span><span class="sxs-lookup"><span data-stu-id="0ed59-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0ed59-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="0ed59-132">TAPI version</span></span><br/> | <span data-ttu-id="0ed59-133">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="0ed59-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="0ed59-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ed59-134">Header</span></span><br/>       | <dl> <span data-ttu-id="0ed59-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ed59-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0ed59-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0ed59-136">Library</span></span><br/>      | <dl> <span data-ttu-id="0ed59-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ed59-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="0ed59-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0ed59-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="0ed59-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ed59-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ed59-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ed59-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ed59-141">**ITAudioSettings**</span><span class="sxs-lookup"><span data-stu-id="0ed59-141">**ITAudioSettings**</span></span>](itaudiosettings.md)
</dt> <dt>

[<span data-ttu-id="0ed59-142">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="0ed59-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="0ed59-143">**AudioSettingsProperty**</span><span class="sxs-lookup"><span data-stu-id="0ed59-143">**AudioSettingsProperty**</span></span>](audiosettingsproperty.md)
</dt> </dl>

 

 




