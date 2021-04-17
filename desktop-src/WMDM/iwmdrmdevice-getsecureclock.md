---
title: IWMDRMDevice GetSecureClock, método
description: El método GetSecureClock recupera el reloj seguro, por lo que se pueden aplicar licencias basadas en el tiempo.
ms.assetid: 6de9b7ce-9c2a-44e5-9de7-40cfbaf4d92c
keywords:
- Método GetSecureClock de Windows Media Administrador de dispositivos
- Método GetSecureClock de Windows Media Administrador de dispositivos, interfaz IWMDRMDevice
- Interfaz IWMDRMDevice de Windows Media Administrador de dispositivos, método GetSecureClock
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClock
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa92c3bc2ee82facf2f2e1043e71467a0c55bd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698512"
---
# <a name="iwmdrmdevicegetsecureclock-method"></a><span data-ttu-id="417ac-106">IWMDRMDevice:: GetSecureClock (método)</span><span class="sxs-lookup"><span data-stu-id="417ac-106">IWMDRMDevice::GetSecureClock method</span></span>

<span data-ttu-id="417ac-107">El método **GetSecureClock** recupera el reloj seguro, por lo que se pueden aplicar licencias basadas en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="417ac-107">The **GetSecureClock** method retrieves the secure clock, so time-based licenses can be enforced.</span></span>

## <a name="syntax"></a><span data-ttu-id="417ac-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="417ac-108">Syntax</span></span>


```C++
HRESULT GetSecureClock(
  [out] BYTE  **ppbSecureClock,
  [out] DWORD *pcbSecureClock,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="417ac-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="417ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="417ac-110">*ppbSecureClock* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="417ac-110">*ppbSecureClock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="417ac-111">Se recuperó el reloj seguro.</span><span class="sxs-lookup"><span data-stu-id="417ac-111">Retrieved secure clock.</span></span>

</dd> <dt>

<span data-ttu-id="417ac-112">*pcbSecureClock* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="417ac-112">*pcbSecureClock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="417ac-113">Tamaño del reloj seguro, en bytes.</span><span class="sxs-lookup"><span data-stu-id="417ac-113">Size of the secure clock, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="417ac-114">*pdwFlags* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="417ac-114">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="417ac-115">Marcas de estado de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="417ac-115">Device status flags.</span></span> <span data-ttu-id="417ac-116">Este valor debe ser uno de los siguientes marcadores.</span><span class="sxs-lookup"><span data-stu-id="417ac-116">This value must be one of the following flags.</span></span>



| <span data-ttu-id="417ac-117">Marca</span><span class="sxs-lookup"><span data-stu-id="417ac-117">Flag</span></span>                     | <span data-ttu-id="417ac-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="417ac-118">Description</span></span>                            |
|--------------------------|----------------------------------------|
| <span data-ttu-id="417ac-119">\_dispositivo \_ ISWMDRM de WMDRM</span><span class="sxs-lookup"><span data-stu-id="417ac-119">WMDRM\_DEVICE\_ISWMDRM</span></span>   | <span data-ttu-id="417ac-120">El dispositivo es compatible con DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="417ac-120">The device supports Windows Media DRM.</span></span> |
| <span data-ttu-id="417ac-121">\_dispositivo \_ NEEDCLOCK de WMDRM</span><span class="sxs-lookup"><span data-stu-id="417ac-121">WMDRM\_DEVICE\_NEEDCLOCK</span></span> | <span data-ttu-id="417ac-122">El dispositivo necesita el reloj.</span><span class="sxs-lookup"><span data-stu-id="417ac-122">The device needs clock.</span></span>                |
| <span data-ttu-id="417ac-123">\_dispositivo WMDRM \_ revocado</span><span class="sxs-lookup"><span data-stu-id="417ac-123">WMDRM\_DEVICE\_REVOKED</span></span>   | <span data-ttu-id="417ac-124">El dispositivo se ha revocado.</span><span class="sxs-lookup"><span data-stu-id="417ac-124">The device has been revoked.</span></span>           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="417ac-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="417ac-125">Return value</span></span>

<span data-ttu-id="417ac-126">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="417ac-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="417ac-127">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="417ac-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="417ac-128">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="417ac-128">Return code</span></span>                                                                          | <span data-ttu-id="417ac-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="417ac-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="417ac-130"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="417ac-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="417ac-131">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="417ac-131">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="417ac-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="417ac-132">Requirements</span></span>



| <span data-ttu-id="417ac-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="417ac-133">Requirement</span></span> | <span data-ttu-id="417ac-134">Value</span><span class="sxs-lookup"><span data-stu-id="417ac-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="417ac-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="417ac-135">Header</span></span><br/>  | <dl> <span data-ttu-id="417ac-136"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="417ac-136"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="417ac-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="417ac-137">Library</span></span><br/> | <dl> <span data-ttu-id="417ac-138"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="417ac-138"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="417ac-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="417ac-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="417ac-140">**GetSecureClockChallenge**</span><span class="sxs-lookup"><span data-stu-id="417ac-140">**GetSecureClockChallenge**</span></span>](iwmdrmdevice-getsecureclockchallenge.md)
</dt> <dt>

[<span data-ttu-id="417ac-141">**Interfaz IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="417ac-141">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> <dt>

[<span data-ttu-id="417ac-142">**SetSecureClockResponse**</span><span class="sxs-lookup"><span data-stu-id="417ac-142">**SetSecureClockResponse**</span></span>](iwmdrmdevice-setsecureclockresponse.md)
</dt> </dl>

 

 





