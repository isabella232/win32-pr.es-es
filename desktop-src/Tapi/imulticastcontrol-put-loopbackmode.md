---
description: El \_ LoopbackMode Put establece el modo de bucle invertido de multidifusión.
ms.assetid: 38b28529-224f-4624-bb5e-22fee500e8e6
title: 'IMulticastControl: método de ut_LoopbackMode de:p (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5b5e51b3814b380cc06d9c960db1a4e4b9ecb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680914"
---
# <a name="imulticastcontrolput_loopbackmode-method"></a><span data-ttu-id="a081f-103">IMulticastControl::p \_ método LoopbackMode UT</span><span class="sxs-lookup"><span data-stu-id="a081f-103">IMulticastControl::put\_LoopbackMode method</span></span>

<span data-ttu-id="a081f-104">\[**colocar \_ LoopbackMode** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a081f-104">\[**put\_LoopbackMode** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a081f-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="a081f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a081f-106">El **\_ LoopbackMode Put** establece el modo de bucle invertido de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="a081f-106">The **put\_LoopbackMode** sets the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="a081f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a081f-107">Syntax</span></span>


```C++
HRESULT put_LoopbackMode(
  [in] MULTICAST_LOOPBACK_MODE mode
);
```



## <a name="parameters"></a><span data-ttu-id="a081f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a081f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a081f-109">*modo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a081f-109">*mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a081f-110">[**Multidifusión \_ \_**](multicast-loopback-mode.md) Descriptor en modo de bucle invertido del nuevo modo de bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="a081f-110">[**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md) descriptor of the new loopback mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a081f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a081f-111">Return value</span></span>

<span data-ttu-id="a081f-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="a081f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="a081f-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a081f-113">Return code</span></span>                                                                                  | <span data-ttu-id="a081f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a081f-114">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="a081f-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a081f-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a081f-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a081f-116">Method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="a081f-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a081f-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a081f-118">El parámetro de *modo* no es válido.</span><span class="sxs-lookup"><span data-stu-id="a081f-118">The *mode* parameter is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a081f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a081f-119">Requirements</span></span>



| <span data-ttu-id="a081f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a081f-120">Requirement</span></span> | <span data-ttu-id="a081f-121">Value</span><span class="sxs-lookup"><span data-stu-id="a081f-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a081f-122">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="a081f-122">TAPI version</span></span><br/> | <span data-ttu-id="a081f-123">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="a081f-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a081f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a081f-124">Header</span></span><br/>       | <dl> <span data-ttu-id="a081f-125"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="a081f-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="a081f-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a081f-126">Library</span></span><br/>      | <dl> <span data-ttu-id="a081f-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a081f-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a081f-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a081f-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="a081f-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a081f-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a081f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a081f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a081f-131">**IMulticastControl**</span><span class="sxs-lookup"><span data-stu-id="a081f-131">**IMulticastControl**</span></span>](imulticastcontrol.md)
</dt> </dl>

 

 




