---
title: Método IWMDRMDeviceApp AcquireDeviceData (WMDRMDeviceApp. h)
description: El método AcquireDeviceData inicializa o restablece el reloj seguro de un dispositivo.
ms.assetid: 2f1cfdb9-0f07-4bee-94aa-b33b039453d0
keywords:
- Método AcquireDeviceData de Windows Media Administrador de dispositivos
- Método AcquireDeviceData de Windows Media Administrador de dispositivos, interfaz IWMDRMDeviceApp
- Interfaz IWMDRMDeviceApp de Windows Media Administrador de dispositivos, método AcquireDeviceData
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.AcquireDeviceData
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 268572e5dad3dffd0fe15956a0ff145f277fb6db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699682"
---
# <a name="iwmdrmdeviceappacquiredevicedata-method"></a><span data-ttu-id="0a1e6-106">IWMDRMDeviceApp:: AcquireDeviceData (método)</span><span class="sxs-lookup"><span data-stu-id="0a1e6-106">IWMDRMDeviceApp::AcquireDeviceData method</span></span>

<span data-ttu-id="0a1e6-107">El método **AcquireDeviceData** inicializa o restablece el reloj seguro de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-107">The **AcquireDeviceData** method initializes or resets a device secure clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a1e6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a1e6-108">Syntax</span></span>


```C++
HRESULT AcquireDeviceData(
  [in]  IWMDMDevice    *pDevice,
  [in]  IWMDMProgress3 *pProgressCallback,
  [in]  DWORD          dwFlags,
  [out] DWORD          *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="0a1e6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a1e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a1e6-110">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0a1e6-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a1e6-111">Puntero a una interfaz [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) para el dispositivo que va a notificar los datos de medición.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface for the device that will report metering data.</span></span>

</dd> <dt>

<span data-ttu-id="0a1e6-112">*pProgressCallback* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0a1e6-112">*pProgressCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a1e6-113">Devolución de llamada de progreso a través de la cual la aplicación puede realizar el seguimiento del progreso del evento o cancelar el evento.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-113">Progress callback through which the application can track the progress of the event, or cancel the event.</span></span> <span data-ttu-id="0a1e6-114">El progreso se identifica mediante el parámetro *EventID* de los métodos [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) .</span><span class="sxs-lookup"><span data-stu-id="0a1e6-114">The progress is identified by the *EventId* parameter of [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) methods.</span></span>

</dd> <dt>

<span data-ttu-id="0a1e6-115">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0a1e6-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a1e6-116">Un **or** lógico de uno o ambos de los siguientes marcadores, que especifican la acción que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-116">A logical **OR** of one or both of the following flags, specifying what action to perform.</span></span> <span data-ttu-id="0a1e6-117">Este valor se recupera del parámetro *pdwStatus* de [**IWMDRMDeviceApp:: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) o [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span><span class="sxs-lookup"><span data-stu-id="0a1e6-117">This value is retrieved from the *pdwStatus* parameter of [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span></span> <span data-ttu-id="0a1e6-118">Puede usar la marca *pdwStatus* directamente.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-118">You can use the *pdwStatus* flag directly.</span></span>



| <span data-ttu-id="0a1e6-119">Marca</span><span class="sxs-lookup"><span data-stu-id="0a1e6-119">Flag</span></span>                        | <span data-ttu-id="0a1e6-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a1e6-120">Description</span></span>                                   |
|-----------------------------|-----------------------------------------------|
| <span data-ttu-id="0a1e6-121">\_dispositivo \_ NEEDCLOCK de WMDRM</span><span class="sxs-lookup"><span data-stu-id="0a1e6-121">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="0a1e6-122">Adquiera un reloj de un servidor de reloj seguro.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-122">Acquire a clock from a secure clock server.</span></span>   |
| <span data-ttu-id="0a1e6-123">\_dispositivo \_ REFRESHCLOCK de WMDRM</span><span class="sxs-lookup"><span data-stu-id="0a1e6-123">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="0a1e6-124">Actualice el reloj desde un servidor de reloj seguro.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-124">Refresh the clock from a secure clock server.</span></span> |



 

</dd> <dt>

<span data-ttu-id="0a1e6-125">*pdwStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0a1e6-125">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a1e6-126">Uno de los siguientes valores **DWORD** que especifican el estado devuelto por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-126">One of the following **DWORD** values specifying the status returned by the device.</span></span>



| <span data-ttu-id="0a1e6-127">Status</span><span class="sxs-lookup"><span data-stu-id="0a1e6-127">Status</span></span> | <span data-ttu-id="0a1e6-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a1e6-128">Description</span></span>                                                     |
|--------|-----------------------------------------------------------------|
| <span data-ttu-id="0a1e6-129">0</span><span class="sxs-lookup"><span data-stu-id="0a1e6-129">0</span></span>      | <span data-ttu-id="0a1e6-130">No se admite la acción.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-130">The action is not supported.</span></span>                                    |
| <span data-ttu-id="0a1e6-131">1</span><span class="sxs-lookup"><span data-stu-id="0a1e6-131">1</span></span>      | <span data-ttu-id="0a1e6-132">No se pudo adquirir el reloj seguro del dispositivo del servicio.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-132">The device secure clock could not be acquired from the service.</span></span> |
| <span data-ttu-id="0a1e6-133">2</span><span class="sxs-lookup"><span data-stu-id="0a1e6-133">2</span></span>      | <span data-ttu-id="0a1e6-134">No se pudo establecer el reloj seguro del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-134">The device's secure clock could not be set.</span></span>                     |
| <span data-ttu-id="0a1e6-135">3</span><span class="sxs-lookup"><span data-stu-id="0a1e6-135">3</span></span>      | <span data-ttu-id="0a1e6-136">Se estableció el reloj seguro del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-136">The device's secure clock was set.</span></span>                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a1e6-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a1e6-137">Return value</span></span>

<span data-ttu-id="0a1e6-138">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-138">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0a1e6-139">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-139">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0a1e6-140">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0a1e6-140">Return code</span></span>                                                                                                                             | <span data-ttu-id="0a1e6-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a1e6-141">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0a1e6-142"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0a1e6-142"><dt>**S\_OK**</dt></span></span> </dl>                                                    | <span data-ttu-id="0a1e6-143">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-143">The method succeeded.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="0a1e6-144"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0a1e6-144"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                                       | <span data-ttu-id="0a1e6-145">Uno o varios argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-145">One or more arguments are not valid.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="0a1e6-146"><dt>**dispositivo \_ E \_ dispositivo \_ no \_ WMDRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0a1e6-146"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl>                        | <span data-ttu-id="0a1e6-147">El dispositivo especificado no es un dispositivo compatible con DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-147">The specified device is not a Windows Media DRM compatible device.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="0a1e6-148"><dt>**\_DRM E \_ DRM \_ no \_ puede \_ obtener \_ el \_ reloj seguro**</dt></span><span class="sxs-lookup"><span data-stu-id="0a1e6-148"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_SECURE\_CLOCK**</dt></span></span> </dl>               | <span data-ttu-id="0a1e6-149">No se pudo recuperar el desafío del reloj seguro del dispositivo o no se pudo recuperar la dirección URL del reloj segura del desafío.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-149">Failed to retrieve secure clock challenge from the device or unable to retrieve the secure clock URL from the challenge.</span></span><br/> |
| <dl> <span data-ttu-id="0a1e6-150"><dt>**\_DRM E \_ DRM \_ no \_ puede \_ obtener \_ el \_ reloj seguro \_ del \_ servidor**</dt></span><span class="sxs-lookup"><span data-stu-id="0a1e6-150"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_SECURE\_CLOCK\_FROM\_SERVER**</dt></span></span> </dl> | <span data-ttu-id="0a1e6-151">No se pudo recuperar la respuesta de reloj segura del servidor de reloj seguro.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-151">Failed to retrieve the secure clock response from the secure clock server.</span></span><br/>                                               |
| <dl> <span data-ttu-id="0a1e6-152"><dt>**\_DRM E \_ DRM \_ no \_ puede \_ establecer \_ el \_ reloj seguro**</dt></span><span class="sxs-lookup"><span data-stu-id="0a1e6-152"><dt>**NS\_E\_DRM\_UNABLE\_TO\_SET\_SECURE\_CLOCK**</dt></span></span> </dl>               | <span data-ttu-id="0a1e6-153">No se pudo enviar el desafío del reloj seguro al dispositivo o el dispositivo no pudo establecer el reloj.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-153">Failed to send the secure clock challenge to the device, or the device failed to set the clock.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="0a1e6-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a1e6-154">Remarks</span></span>

<span data-ttu-id="0a1e6-155">Se trata de un método asincrónico; el dispositivo debe esperar la devolución de llamada [**IWMDMProgress:: end**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) para esta operación antes de intentar reproducir cualquier contenido con licencia.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-155">This is an asynchronous method; the device must await the [**IWMDMProgress::End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) callback for this operation before attempting to play any licensed content.</span></span>

<span data-ttu-id="0a1e6-156">Una aplicación puede aprender si el dispositivo debe restablecer su reloj o actualizarse llamando a [**IWMDRMDeviceApp:: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) o [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span><span class="sxs-lookup"><span data-stu-id="0a1e6-156">An application can learn if the device must have its clock reset or updated by calling [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span></span>

<span data-ttu-id="0a1e6-157">La aplicación debe tener una conexión a Internet para que pueda adquirir o restablecer un reloj seguro.</span><span class="sxs-lookup"><span data-stu-id="0a1e6-157">Your application must have an Internet connection to enable it to acquire or reset a secure clock.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a1e6-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a1e6-158">Requirements</span></span>



| <span data-ttu-id="0a1e6-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a1e6-159">Requirement</span></span> | <span data-ttu-id="0a1e6-160">Value</span><span class="sxs-lookup"><span data-stu-id="0a1e6-160">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a1e6-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a1e6-161">Header</span></span><br/>  | <dl> <span data-ttu-id="0a1e6-162"><dt>WMDRMDeviceApp. h (también requiere Wmdrmdeviceapp \_ i, generado a partir de WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="0a1e6-162"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="0a1e6-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0a1e6-163">Library</span></span><br/> | <dl> <span data-ttu-id="0a1e6-164"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a1e6-164"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="0a1e6-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a1e6-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a1e6-166">**Control del contenido protegido en la aplicación**</span><span class="sxs-lookup"><span data-stu-id="0a1e6-166">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="0a1e6-167">**Interfaz IWMDMDevice**</span><span class="sxs-lookup"><span data-stu-id="0a1e6-167">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="0a1e6-168">**Interfaz IWMDMProgress3**</span><span class="sxs-lookup"><span data-stu-id="0a1e6-168">**IWMDMProgress3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[<span data-ttu-id="0a1e6-169">**Interfaz IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="0a1e6-169">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





