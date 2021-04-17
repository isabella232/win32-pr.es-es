---
description: El método Set establece el valor de una propiedad de control de calidad de llamada determinada.
ms.assetid: e83ed9d7-0a53-4555-ae44-737ab3dfb749
title: 'ITCallQualityControl:: set (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c0a83702ba0dd4d04eb129eeed95c46d2a79a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680210"
---
# <a name="itcallqualitycontrolset-method"></a><span data-ttu-id="aaef4-103">ITCallQualityControl:: set (método)</span><span class="sxs-lookup"><span data-stu-id="aaef4-103">ITCallQualityControl::Set method</span></span>

<span data-ttu-id="aaef4-104">\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="aaef4-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="aaef4-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="aaef4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="aaef4-106">El método **set** establece el valor de una [propiedad de control de calidad de llamada](callqualityproperty.md)determinada.</span><span class="sxs-lookup"><span data-stu-id="aaef4-106">The **Set** method sets the value of a given [call quality control property](callqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="aaef4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aaef4-107">Syntax</span></span>


```C++
HRESULT Set(
  [in] CallQualityProperty Property,
  [in] long                lValue,
  [in] TAPIControlFlags    lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="aaef4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aaef4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaef4-109">*Propiedad* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aaef4-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaef4-110">Miembro de la enumeración [**CallQualityProperty**](callqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="aaef4-110">Member of the [**CallQualityProperty**](callqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="aaef4-111">valor *l* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aaef4-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaef4-112">Valor deseado para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="aaef4-112">Desired value for the property.</span></span>

</dd> <dt>

<span data-ttu-id="aaef4-113">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aaef4-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaef4-114">Valor de la enumeración [**TAPIControlFlags**](tapicontrolflags.md) que indica cómo se controlará el valor de la *propiedad* .</span><span class="sxs-lookup"><span data-stu-id="aaef4-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaef4-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aaef4-115">Return value</span></span>

<span data-ttu-id="aaef4-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="aaef4-116">This method can return one of these values.</span></span>



| <span data-ttu-id="aaef4-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="aaef4-117">Return code</span></span>                                                                                   | <span data-ttu-id="aaef4-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="aaef4-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="aaef4-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="aaef4-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="aaef4-120">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="aaef4-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="aaef4-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="aaef4-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="aaef4-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="aaef4-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="aaef4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aaef4-123">Requirements</span></span>



| <span data-ttu-id="aaef4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="aaef4-124">Requirement</span></span> | <span data-ttu-id="aaef4-125">Value</span><span class="sxs-lookup"><span data-stu-id="aaef4-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aaef4-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="aaef4-126">TAPI version</span></span><br/> | <span data-ttu-id="aaef4-127">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="aaef4-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="aaef4-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aaef4-128">Header</span></span><br/>       | <dl> <span data-ttu-id="aaef4-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="aaef4-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="aaef4-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aaef4-130">Library</span></span><br/>      | <dl> <span data-ttu-id="aaef4-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aaef4-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="aaef4-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aaef4-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="aaef4-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aaef4-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaef4-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="aaef4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaef4-135">**ITCallQualityControl**</span><span class="sxs-lookup"><span data-stu-id="aaef4-135">**ITCallQualityControl**</span></span>](itcallqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="aaef4-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="aaef4-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="aaef4-137">**CallQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="aaef4-137">**CallQualityProperty**</span></span>](callqualityproperty.md)
</dt> </dl>

 

 




