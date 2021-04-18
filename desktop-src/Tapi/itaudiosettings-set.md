---
description: El método Set establece el valor de una propiedad de configuración de audio determinada.
ms.assetid: 3132e004-5543-4b21-878d-35197f7077d6
title: 'ITAudioSettings:: set (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf947c28d3b5270b3c5dabd4196d0e6b71f57911
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680911"
---
# <a name="itaudiosettingsset-method"></a><span data-ttu-id="d64e7-103">ITAudioSettings:: set (método)</span><span class="sxs-lookup"><span data-stu-id="d64e7-103">ITAudioSettings::Set method</span></span>

<span data-ttu-id="d64e7-104">\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d64e7-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d64e7-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="d64e7-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d64e7-106">El método **set** establece el valor de una [**propiedad de configuración de audio**](audiosettingsproperty.md)determinada.</span><span class="sxs-lookup"><span data-stu-id="d64e7-106">The **Set** method sets the value of a given [**audio settings property**](audiosettingsproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d64e7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d64e7-107">Syntax</span></span>


```C++
HRESULT get_Error(
  [out] HRESULT *phrErrorCode
);
```



## <a name="parameters"></a><span data-ttu-id="d64e7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d64e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d64e7-109">*Propiedad* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d64e7-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d64e7-110">Miembro de la enumeración [**AudioSettingsProperty**](audiosettingsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="d64e7-110">Member of the [**AudioSettingsProperty**](audiosettingsproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="d64e7-111">valor *l* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d64e7-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d64e7-112">Valor deseado para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d64e7-112">Desired value for the property.</span></span>

</dd> <dt>

<span data-ttu-id="d64e7-113">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d64e7-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d64e7-114">Valor de la enumeración [**TAPIControlFlags**](tapicontrolflags.md) que indica cómo se controlará el valor de la *propiedad* .</span><span class="sxs-lookup"><span data-stu-id="d64e7-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d64e7-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d64e7-115">Return value</span></span>

<span data-ttu-id="d64e7-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="d64e7-116">This method can return one of these values.</span></span>



| <span data-ttu-id="d64e7-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d64e7-117">Return code</span></span>                                                                                   | <span data-ttu-id="d64e7-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="d64e7-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="d64e7-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d64e7-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d64e7-120">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d64e7-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d64e7-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d64e7-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d64e7-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="d64e7-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d64e7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d64e7-123">Requirements</span></span>



| <span data-ttu-id="d64e7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d64e7-124">Requirement</span></span> | <span data-ttu-id="d64e7-125">Value</span><span class="sxs-lookup"><span data-stu-id="d64e7-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d64e7-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="d64e7-126">TAPI version</span></span><br/> | <span data-ttu-id="d64e7-127">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="d64e7-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="d64e7-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d64e7-128">Header</span></span><br/>       | <dl> <span data-ttu-id="d64e7-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d64e7-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d64e7-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d64e7-130">Library</span></span><br/>      | <dl> <span data-ttu-id="d64e7-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d64e7-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="d64e7-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d64e7-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="d64e7-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d64e7-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d64e7-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="d64e7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d64e7-135">**ITAudioSettings**</span><span class="sxs-lookup"><span data-stu-id="d64e7-135">**ITAudioSettings**</span></span>](itaudiosettings.md)
</dt> <dt>

[<span data-ttu-id="d64e7-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="d64e7-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="d64e7-137">**AudioSettingsProperty**</span><span class="sxs-lookup"><span data-stu-id="d64e7-137">**AudioSettingsProperty**</span></span>](audiosettingsproperty.md)
</dt> </dl>

 

 




