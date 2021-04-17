---
title: IWMDRMDevice GetMeterChallenge, método
description: El método GetMeterChallenge recupera el desafío de medición.
ms.assetid: 4c122886-46bd-4e63-8e7d-5e6132363662
keywords:
- Método GetMeterChallenge de Windows Media Administrador de dispositivos
- Método GetMeterChallenge de Windows Media Administrador de dispositivos, interfaz IWMDRMDevice
- Interfaz IWMDRMDevice de Windows Media Administrador de dispositivos, método GetMeterChallenge
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a916afa90d1db310041f9b92be94d3af9154df4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698515"
---
# <a name="iwmdrmdevicegetmeterchallenge-method"></a><span data-ttu-id="0c39d-106">IWMDRMDevice:: GetMeterChallenge (método)</span><span class="sxs-lookup"><span data-stu-id="0c39d-106">IWMDRMDevice::GetMeterChallenge method</span></span>

<span data-ttu-id="0c39d-107">El método **GetMeterChallenge** recupera el desafío de medición.</span><span class="sxs-lookup"><span data-stu-id="0c39d-107">The **GetMeterChallenge** method retrieves the metering challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c39d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c39d-108">Syntax</span></span>


```C++
HRESULT GetMeterChallenge(
  [in]  BSTR  bstrMeterCert,
  [out] BYTE  **ppbMeterChallenge,
  [out] DWORD *pcbMeterChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="0c39d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c39d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c39d-110">*bstrMeterCert* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c39d-110">*bstrMeterCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c39d-111">Certificado de medición que el propietario del contenido envía al equipo host para recopilar los datos de medición asociados en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="0c39d-111">Metering certificate that the content owner sends to the host computer for collecting the associated metering data on the device</span></span>

</dd> <dt>

<span data-ttu-id="0c39d-112">*ppbMeterChallenge* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0c39d-112">*ppbMeterChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c39d-113">Resultado de desafío de medición recuperado.</span><span class="sxs-lookup"><span data-stu-id="0c39d-113">Retrieved metering challenge result.</span></span>

</dd> <dt>

<span data-ttu-id="0c39d-114">*pcbMeterChallenge* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0c39d-114">*pcbMeterChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c39d-115">Tamaño del desafío de medición, en bytes.</span><span class="sxs-lookup"><span data-stu-id="0c39d-115">The size of the metering challenge, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c39d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c39d-116">Return value</span></span>

<span data-ttu-id="0c39d-117">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0c39d-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0c39d-118">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="0c39d-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0c39d-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0c39d-119">Return code</span></span>                                                                          | <span data-ttu-id="0c39d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c39d-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0c39d-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0c39d-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0c39d-122">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="0c39d-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0c39d-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c39d-123">Remarks</span></span>

<span data-ttu-id="0c39d-124">Los datos de medición se recopilan y almacenan en el almacén de datos DRM en el dispositivo para el contenido con la medición habilitada.</span><span class="sxs-lookup"><span data-stu-id="0c39d-124">Metering data is collected and stored in the DRM data store on the device for content with metering enabled.</span></span> <span data-ttu-id="0c39d-125">Se registrarán acciones como Play.</span><span class="sxs-lookup"><span data-stu-id="0c39d-125">Actions such as play will be recorded.</span></span> <span data-ttu-id="0c39d-126">Cuando se llama a esta función, el dispositivo recopila los datos de medición en el almacén de datos DRM en forma de un documento XML y lo envía a hostcomputer.</span><span class="sxs-lookup"><span data-stu-id="0c39d-126">When this function is called, the device collects the metering data in the DRM data store in the form of an XML document and sends it to the hostcomputer.</span></span> <span data-ttu-id="0c39d-127">Si hay demasiados datos, se envían en fases.</span><span class="sxs-lookup"><span data-stu-id="0c39d-127">If there is too much data, it is sent in phases.</span></span>

<span data-ttu-id="0c39d-128">Cuando el equipo host recibe los datos de medición, envía los datos a través de Internet a la dirección URL especificada en el certificado de medición.</span><span class="sxs-lookup"><span data-stu-id="0c39d-128">When the host computer receives the metering data, it sends the data over the Internet to the URL specified in the metering certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c39d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c39d-129">Requirements</span></span>



| <span data-ttu-id="0c39d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c39d-130">Requirement</span></span> | <span data-ttu-id="0c39d-131">Value</span><span class="sxs-lookup"><span data-stu-id="0c39d-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c39d-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c39d-132">Header</span></span><br/>  | <dl> <span data-ttu-id="0c39d-133"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0c39d-133"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="0c39d-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c39d-134">Library</span></span><br/> | <dl> <span data-ttu-id="0c39d-135"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c39d-135"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c39d-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c39d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c39d-137">**Interfaz IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="0c39d-137">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





