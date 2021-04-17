---
description: El \_ método get LoopbackMode obtiene el modo de bucle invertido de multidifusión.
ms.assetid: 2499c108-f70b-4afe-aa2b-2376c95b84bd
title: 'Método IMulticastControl:: get_LoopbackMode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 203d68f5b620ddf5e5ce7a36e4f8b85820deab2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690316"
---
# <a name="imulticastcontrolget_loopbackmode-method"></a><span data-ttu-id="d7bfa-103">IMulticastControl:: get \_ LoopbackMode (método)</span><span class="sxs-lookup"><span data-stu-id="d7bfa-103">IMulticastControl::get\_LoopbackMode method</span></span>

<span data-ttu-id="d7bfa-104">\[**obtener \_ LoopbackMode** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d7bfa-104">\[**get\_LoopbackMode** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d7bfa-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="d7bfa-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d7bfa-106">El método **Get \_ LoopbackMode** obtiene el modo de bucle invertido de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="d7bfa-106">The **get\_LoopbackMode** method gets the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7bfa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7bfa-107">Syntax</span></span>


```C++
HRESULT get_LoopbackMode(
  [out] MULTICAST_LOOPBACK_MODE *pMode
);
```



## <a name="parameters"></a><span data-ttu-id="d7bfa-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7bfa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7bfa-109">*pMode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d7bfa-109">*pMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7bfa-110">Puntero al descriptor del [**\_ \_ modo de bucle invertido de multidifusión**](multicast-loopback-mode.md) del modo de bucle invertido actual.</span><span class="sxs-lookup"><span data-stu-id="d7bfa-110">Pointer to the [**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md) descriptor of the current loopback mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7bfa-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7bfa-111">Return value</span></span>

<span data-ttu-id="d7bfa-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="d7bfa-112">This method can return one of these values.</span></span>



| <span data-ttu-id="d7bfa-113">Value</span><span class="sxs-lookup"><span data-stu-id="d7bfa-113">Value</span></span>                                                                                        | <span data-ttu-id="d7bfa-114">Significado</span><span class="sxs-lookup"><span data-stu-id="d7bfa-114">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="d7bfa-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d7bfa-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d7bfa-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d7bfa-116">Method succeeded.</span></span><br/>                   |
| <dl> <span data-ttu-id="d7bfa-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d7bfa-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="d7bfa-118">El parámetro *pMode* no es válido.</span><span class="sxs-lookup"><span data-stu-id="d7bfa-118">The *pMode* parameter is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d7bfa-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7bfa-119">Requirements</span></span>



| <span data-ttu-id="d7bfa-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7bfa-120">Requirement</span></span> | <span data-ttu-id="d7bfa-121">Value</span><span class="sxs-lookup"><span data-stu-id="d7bfa-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7bfa-122">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="d7bfa-122">TAPI version</span></span><br/> | <span data-ttu-id="d7bfa-123">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="d7bfa-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d7bfa-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7bfa-124">Header</span></span><br/>       | <dl> <span data-ttu-id="d7bfa-125"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7bfa-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="d7bfa-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7bfa-126">Library</span></span><br/>      | <dl> <span data-ttu-id="d7bfa-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7bfa-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d7bfa-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d7bfa-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="d7bfa-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7bfa-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d7bfa-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7bfa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7bfa-131">**IMulticastControl**</span><span class="sxs-lookup"><span data-stu-id="d7bfa-131">**IMulticastControl**</span></span>](imulticastcontrol.md)
</dt> </dl>

 

 




