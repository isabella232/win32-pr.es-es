---
title: IWMDRMDevice SetMeterResponse, método
description: El método SetMeterResponse establece la respuesta de medición.
ms.assetid: 3f2e7d7c-6470-4d53-96b0-d3eebdb08329
keywords:
- Método SetMeterResponse de Windows Media Administrador de dispositivos
- Método SetMeterResponse de Windows Media Administrador de dispositivos, interfaz IWMDRMDevice
- Interfaz IWMDRMDevice de Windows Media Administrador de dispositivos, método SetMeterResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed70b158215eb831296ad083af8cd2c001cb38f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699608"
---
# <a name="iwmdrmdevicesetmeterresponse-method"></a><span data-ttu-id="23f50-106">IWMDRMDevice:: SetMeterResponse (método)</span><span class="sxs-lookup"><span data-stu-id="23f50-106">IWMDRMDevice::SetMeterResponse method</span></span>

<span data-ttu-id="23f50-107">El método **SetMeterResponse** establece la respuesta de medición.</span><span class="sxs-lookup"><span data-stu-id="23f50-107">The **SetMeterResponse** method sets the metering response.</span></span>

## <a name="syntax"></a><span data-ttu-id="23f50-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23f50-108">Syntax</span></span>


```C++
HRESULT SetMeterResponse(
  [in]  BYTE  *pbMeterResponse,
  [in]  DWORD cbMeterResponse,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="23f50-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23f50-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23f50-110">*pbMeterResponse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="23f50-110">*pbMeterResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23f50-111">Respuesta de medición que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="23f50-111">The metering response to be set.</span></span>

</dd> <dt>

<span data-ttu-id="23f50-112">*cbMeterResponse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="23f50-112">*cbMeterResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23f50-113">Tamaño de la respuesta de medición, en bytes.</span><span class="sxs-lookup"><span data-stu-id="23f50-113">Size of the metering response, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="23f50-114">*pdwFlags* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="23f50-114">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23f50-115">Marcas de respuesta.</span><span class="sxs-lookup"><span data-stu-id="23f50-115">Response flags.</span></span> <span data-ttu-id="23f50-116">Este valor debe ser uno de los siguientes marcadores.</span><span class="sxs-lookup"><span data-stu-id="23f50-116">This value must be one of the following flags.</span></span>



| <span data-ttu-id="23f50-117">Marca</span><span class="sxs-lookup"><span data-stu-id="23f50-117">Flag</span></span>                            | <span data-ttu-id="23f50-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="23f50-118">Description</span></span>              |
|---------------------------------|--------------------------|
| <span data-ttu-id="23f50-119">\_respuesta del medidor de WMDRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="23f50-119">WMDRM\_METER\_RESPONSE\_ALL</span></span>     | <span data-ttu-id="23f50-120">Todas las respuestas de medición.</span><span class="sxs-lookup"><span data-stu-id="23f50-120">All meter responses.</span></span>     |
| <span data-ttu-id="23f50-121">respuesta de medidor de WMDRM \_ \_ \_ parcial</span><span class="sxs-lookup"><span data-stu-id="23f50-121">WMDRM\_METER\_RESPONSE\_PARTIAL</span></span> | <span data-ttu-id="23f50-122">Respuestas de medidores parciales.</span><span class="sxs-lookup"><span data-stu-id="23f50-122">Partial meter responses.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23f50-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23f50-123">Return value</span></span>

<span data-ttu-id="23f50-124">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="23f50-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="23f50-125">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="23f50-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="23f50-126">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="23f50-126">Return code</span></span>                                                                          | <span data-ttu-id="23f50-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="23f50-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="23f50-128"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="23f50-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="23f50-129">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="23f50-129">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="23f50-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23f50-130">Requirements</span></span>



| <span data-ttu-id="23f50-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="23f50-131">Requirement</span></span> | <span data-ttu-id="23f50-132">Value</span><span class="sxs-lookup"><span data-stu-id="23f50-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23f50-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23f50-133">Header</span></span><br/>  | <dl> <span data-ttu-id="23f50-134"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="23f50-134"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="23f50-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23f50-135">Library</span></span><br/> | <dl> <span data-ttu-id="23f50-136"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23f50-136"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23f50-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="23f50-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23f50-138">**Interfaz IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="23f50-138">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





