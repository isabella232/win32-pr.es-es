---
title: Método IWMDRMDeviceApp ProcessMeterResponse (WMDRMDeviceApp. h)
description: El método ProcessMeterResponse restablece algunos o todos los recuentos de disponibilidad en un dispositivo, después de que el servidor haya enviado y procesado los datos del dispositivo.
ms.assetid: bafc4bb2-aa3c-4b2a-a818-1a78577cefc5
keywords:
- Método ProcessMeterResponse de Windows Media Administrador de dispositivos
- Método ProcessMeterResponse de Windows Media Administrador de dispositivos, interfaz IWMDRMDeviceApp
- Interfaz IWMDRMDeviceApp de Windows Media Administrador de dispositivos, método ProcessMeterResponse
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.ProcessMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b57312dc2f401207e41f38f5bf75cddf69a13b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699680"
---
# <a name="iwmdrmdeviceappprocessmeterresponse-method"></a><span data-ttu-id="b5437-106">IWMDRMDeviceApp::P método rocessMeterResponse</span><span class="sxs-lookup"><span data-stu-id="b5437-106">IWMDRMDeviceApp::ProcessMeterResponse method</span></span>

<span data-ttu-id="b5437-107">El método **ProcessMeterResponse** restablece algunos o todos los recuentos de disponibilidad en un dispositivo, después de que el servidor haya enviado y procesado los datos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b5437-107">The **ProcessMeterResponse** method resets some or all of the metering counts on a device, after data from the device has been sent to and processed by the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5437-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5437-108">Syntax</span></span>


```C++
HRESULT ProcessMeterResponse(
  [in]  IWMDMDevice *pDevice,
  [in]  BYTE        *pbResponse,
  [in]  DWORD       cbResponse,
  [out] DWORD       *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b5437-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5437-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5437-110">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5437-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5437-111">Puntero a un objeto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="b5437-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="b5437-112">*pbResponse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5437-112">*pbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5437-113">Respuesta recibida de un servidor de disponibilidad, después de enviar los datos generados con [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).</span><span class="sxs-lookup"><span data-stu-id="b5437-113">Response received from a metering server, after sending data generated using [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5437-114">*cbResponse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5437-114">*cbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5437-115">Tamaño de *pbResponse*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b5437-115">Size of *pbResponse*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b5437-116">*pdwFlags* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b5437-116">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5437-117">Un **valor DWORD** de la siguiente tabla que indica si hay más datos de disponibilidad en el dispositivo que se deben procesar.</span><span class="sxs-lookup"><span data-stu-id="b5437-117">A **DWORD** from the following table indicating whether there is more metering data on the device that needs to be processed.</span></span>



| <span data-ttu-id="b5437-118">Marca</span><span class="sxs-lookup"><span data-stu-id="b5437-118">Flag</span></span>                            | <span data-ttu-id="b5437-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5437-119">Description</span></span>                                     |
|---------------------------------|-------------------------------------------------|
| <span data-ttu-id="b5437-120">\_respuesta del medidor de WMDRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="b5437-120">WMDRM\_METER\_RESPONSE\_ALL</span></span>     | <span data-ttu-id="b5437-121">Se han procesado todos los datos de medición.</span><span class="sxs-lookup"><span data-stu-id="b5437-121">All metering data has been processed.</span></span>           |
| <span data-ttu-id="b5437-122">respuesta de medidor de WMDRM \_ \_ \_ parcial</span><span class="sxs-lookup"><span data-stu-id="b5437-122">WMDRM\_METER\_RESPONSE\_PARTIAL</span></span> | <span data-ttu-id="b5437-123">Es necesario procesar datos de medición adicionales.</span><span class="sxs-lookup"><span data-stu-id="b5437-123">Additional metering data needs to be processed.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5437-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5437-124">Return value</span></span>

<span data-ttu-id="b5437-125">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b5437-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b5437-126">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="b5437-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b5437-127">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b5437-127">Return code</span></span>                                                                                                      | <span data-ttu-id="b5437-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5437-128">Description</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5437-129"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b5437-129"><dt>**S\_OK**</dt></span></span> </dl>                             | <span data-ttu-id="b5437-130">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="b5437-130">The method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="b5437-131"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b5437-131"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="b5437-132">Uno o varios argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="b5437-132">One or more arguments are not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="b5437-133"><dt>**Errores del dispositivo**</dt></span><span class="sxs-lookup"><span data-stu-id="b5437-133"><dt>**Errors from the device**</dt></span></span> </dl>            | <span data-ttu-id="b5437-134">Cualquier número de errores de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b5437-134">Any of a number of device errors.</span></span><br/>                                  |
| <dl> <span data-ttu-id="b5437-135"><dt>**Errores del cliente DRM**</dt></span><span class="sxs-lookup"><span data-stu-id="b5437-135"><dt>**Errors from the DRM Client**</dt></span></span> </dl>        | <span data-ttu-id="b5437-136">Cualquiera de los errores internos del cliente DRM.</span><span class="sxs-lookup"><span data-stu-id="b5437-136">Any of a number of internal DRM client errors.</span></span><br/>                     |
| <dl> <span data-ttu-id="b5437-137"><dt>**dispositivo \_ E \_ dispositivo \_ no \_ WMDRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5437-137"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl> | <span data-ttu-id="b5437-138">El dispositivo especificado no es un dispositivo compatible con DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b5437-138">The specified device is not a Windows Media DRM compatible device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b5437-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5437-139">Remarks</span></span>

<span data-ttu-id="b5437-140">Puede encontrar más información sobre la medición, incluidos ejemplos de código, en las notas del producto sobre [el uso de contenido multimedia digital con Windows Media DRM 10](/previous-versions//bb614723(v=vs.85)) en el sitio web de MSDN.</span><span class="sxs-lookup"><span data-stu-id="b5437-140">More information on metering, including code examples, can be found in the whitepaper [Metering the Use of Digital Media Content with Windows Media DRM 10](/previous-versions//bb614723(v=vs.85)) on the MSDN Web site.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5437-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5437-141">Requirements</span></span>



| <span data-ttu-id="b5437-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5437-142">Requirement</span></span> | <span data-ttu-id="b5437-143">Value</span><span class="sxs-lookup"><span data-stu-id="b5437-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5437-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5437-144">Header</span></span><br/>  | <dl> <span data-ttu-id="b5437-145"><dt>WMDRMDeviceApp. h (también requiere Wmdrmdeviceapp \_ i, generado a partir de WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="b5437-145"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="b5437-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5437-146">Library</span></span><br/> | <dl> <span data-ttu-id="b5437-147"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5437-147"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="b5437-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5437-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5437-149">**Control del contenido protegido en la aplicación**</span><span class="sxs-lookup"><span data-stu-id="b5437-149">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="b5437-150">**Interfaz IWMDMDevice**</span><span class="sxs-lookup"><span data-stu-id="b5437-150">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="b5437-151">**Interfaz IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="b5437-151">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

