---
description: El método Set establece el valor de una propiedad de calidad de flujo determinada.
ms.assetid: 57029d1c-ac63-45c0-9d07-43c7b46a27b1
title: 'ITStreamQualityControl:: set (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61deed4d6edc9b08d7c11fcc8d44d8cf91e11f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680296"
---
# <a name="itstreamqualitycontrolset-method"></a><span data-ttu-id="b56f1-103">ITStreamQualityControl:: set (método)</span><span class="sxs-lookup"><span data-stu-id="b56f1-103">ITStreamQualityControl::Set method</span></span>

<span data-ttu-id="b56f1-104">\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b56f1-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b56f1-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="b56f1-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b56f1-106">El método **set** establece el valor de una [**propiedad de calidad de flujo**](streamqualityproperty.md)determinada.</span><span class="sxs-lookup"><span data-stu-id="b56f1-106">The **Set** method sets the value of a given [**stream quality property**](streamqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b56f1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b56f1-107">Syntax</span></span>


```C++
HRESULT Set(
  [in] StreamQualityProperty Property,
  [in] long                  lValue,
  [in] TAPIControlFlags      lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b56f1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b56f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b56f1-109">*Propiedad* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b56f1-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b56f1-110">Miembro de la enumeración [**StreamQualityProperty**](streamqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="b56f1-110">Member of the [**StreamQualityProperty**](streamqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="b56f1-111">valor *l* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b56f1-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b56f1-112">Valor deseado para la *propiedad* de entrada.</span><span class="sxs-lookup"><span data-stu-id="b56f1-112">Desired value for the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="b56f1-113">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b56f1-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b56f1-114">Valor de la enumeración [**TAPIControlFlags**](tapicontrolflags.md) que indica cómo se controlará el valor de la *propiedad* .</span><span class="sxs-lookup"><span data-stu-id="b56f1-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b56f1-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b56f1-115">Return value</span></span>

<span data-ttu-id="b56f1-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="b56f1-116">This method can return one of these values.</span></span>



| <span data-ttu-id="b56f1-117">Value</span><span class="sxs-lookup"><span data-stu-id="b56f1-117">Value</span></span>                                                                                         | <span data-ttu-id="b56f1-118">Significado</span><span class="sxs-lookup"><span data-stu-id="b56f1-118">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b56f1-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b56f1-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b56f1-120">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b56f1-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b56f1-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b56f1-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b56f1-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="b56f1-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b56f1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b56f1-123">Requirements</span></span>



| <span data-ttu-id="b56f1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b56f1-124">Requirement</span></span> | <span data-ttu-id="b56f1-125">Value</span><span class="sxs-lookup"><span data-stu-id="b56f1-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b56f1-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="b56f1-126">TAPI version</span></span><br/> | <span data-ttu-id="b56f1-127">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="b56f1-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="b56f1-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b56f1-128">Header</span></span><br/>       | <dl> <span data-ttu-id="b56f1-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b56f1-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b56f1-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b56f1-130">Library</span></span><br/>      | <dl> <span data-ttu-id="b56f1-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b56f1-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="b56f1-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b56f1-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="b56f1-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b56f1-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b56f1-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="b56f1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b56f1-135">**ITStreamQualityControl**</span><span class="sxs-lookup"><span data-stu-id="b56f1-135">**ITStreamQualityControl**</span></span>](itstreamqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="b56f1-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="b56f1-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="b56f1-137">**StreamQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="b56f1-137">**StreamQualityProperty**</span></span>](streamqualityproperty.md)
</dt> </dl>

 

 




