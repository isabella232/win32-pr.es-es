---
title: Método IWMDRMDeviceApp GenerateMeterChallenge (WMDRMDeviceApp. h)
description: El método GenerateMeterChallenge adquiere datos de medición de un dispositivo.
ms.assetid: 2457cab7-bd45-49a7-ba69-74ae022207ce
keywords:
- Método GenerateMeterChallenge de Windows Media Administrador de dispositivos
- Método GenerateMeterChallenge de Windows Media Administrador de dispositivos, interfaz IWMDRMDeviceApp
- Interfaz IWMDRMDeviceApp de Windows Media Administrador de dispositivos, método GenerateMeterChallenge
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.GenerateMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a71f04a5837f09575a2f4bccf4b17e34e30d63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699681"
---
# <a name="iwmdrmdeviceappgeneratemeterchallenge-method"></a><span data-ttu-id="10820-106">IWMDRMDeviceApp:: GenerateMeterChallenge (método)</span><span class="sxs-lookup"><span data-stu-id="10820-106">IWMDRMDeviceApp::GenerateMeterChallenge method</span></span>

<span data-ttu-id="10820-107">El método **GenerateMeterChallenge** adquiere datos de medición de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10820-107">The **GenerateMeterChallenge** method acquires metering data from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="10820-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10820-108">Syntax</span></span>


```C++
HRESULT GenerateMeterChallenge(
  [in]  IWMDMDevice *pDevice,
  [in]  BSTR        bstrMeterCert,
  [out] BSTR        *pbstrMeterURL,
  [out] BSTR        *pbstrMeterData
);
```



## <a name="parameters"></a><span data-ttu-id="10820-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10820-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10820-110">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="10820-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10820-111">Puntero a una interfaz [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="10820-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface.</span></span> <span data-ttu-id="10820-112">Si la aplicación pasa a ser **null**, se usa la información de disponibilidad almacenada en el equipo en lugar de la información de disponibilidad de un dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="10820-112">If the application passes in **NULL**, metering information stored on the computer is used instead of metering information from a connected device.</span></span>

</dd> <dt>

<span data-ttu-id="10820-113">*bstrMeterCert* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="10820-113">*bstrMeterCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10820-114">El certificado de medición de la aplicación, como **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="10820-114">The application's metering certificate, as a **BSTR**.</span></span> <span data-ttu-id="10820-115">Se trata de un certificado firmado recibido de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="10820-115">This is a signed certificate received from Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="10820-116">*pbstrMeterURL* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="10820-116">*pbstrMeterURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10820-117">Dirección URL a la que se deben enviar los datos de medición.</span><span class="sxs-lookup"><span data-stu-id="10820-117">The URL where metering data should be sent.</span></span> <span data-ttu-id="10820-118">Lo asigna el Administrador de dispositivos de Windows Media, y el llamador debe liberarlo mediante el uso de **SysFreeString**.</span><span class="sxs-lookup"><span data-stu-id="10820-118">This is allocated by Windows Media Device Manager, and must be free by the caller using **SysFreeString**.</span></span>

</dd> <dt>

<span data-ttu-id="10820-119">*pbstrMeterData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="10820-119">*pbstrMeterData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10820-120">Medición de los datos que se van a enviar al servicio de medición.</span><span class="sxs-lookup"><span data-stu-id="10820-120">Metering data to send to the metering service.</span></span> <span data-ttu-id="10820-121">Lo asigna el Administrador de dispositivos de Windows Media, y el llamador debe liberarlo mediante el uso de **SysFreeString**.</span><span class="sxs-lookup"><span data-stu-id="10820-121">This is allocated by Windows Media Device Manager, and must be free by the caller using **SysFreeString**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10820-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10820-122">Return value</span></span>

<span data-ttu-id="10820-123">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="10820-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="10820-124">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="10820-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="10820-125">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="10820-125">Return code</span></span>                                                                                                      | <span data-ttu-id="10820-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="10820-126">Description</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="10820-127"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="10820-127"><dt>**S\_OK**</dt></span></span> </dl>                             | <span data-ttu-id="10820-128">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="10820-128">The method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="10820-129"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="10820-129"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="10820-130">Uno o varios argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="10820-130">One or more arguments are not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="10820-131"><dt>**DRM \_ E \_ INVALIDXMLTAG**</dt></span><span class="sxs-lookup"><span data-stu-id="10820-131"><dt>**DRM\_E\_INVALIDXMLTAG**</dt></span></span> </dl>             | <span data-ttu-id="10820-132">XML tiene un formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="10820-132">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="10820-133"><dt>**DRM \_ E \_ NOXMLCLOSETAG**</dt></span><span class="sxs-lookup"><span data-stu-id="10820-133"><dt>**DRM\_E\_NOXMLCLOSETAG**</dt></span></span> </dl>             | <span data-ttu-id="10820-134">XML tiene un formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="10820-134">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="10820-135"><dt>**DRM \_ E \_ NOXMLOPENTAG**</dt></span><span class="sxs-lookup"><span data-stu-id="10820-135"><dt>**DRM\_E\_NOXMLOPENTAG**</dt></span></span> </dl>              | <span data-ttu-id="10820-136">XML tiene un formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="10820-136">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="10820-137"><dt>**DRM \_ E \_ XMLNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="10820-137"><dt>**DRM\_E\_XMLNOTFOUND**</dt></span></span> </dl>               | <span data-ttu-id="10820-138">No se pudo encontrar una etiqueta XML requerida.</span><span class="sxs-lookup"><span data-stu-id="10820-138">Failed to find a required XML tag.</span></span><br/>                                 |
| <dl> <span data-ttu-id="10820-139"><dt>**Errores del dispositivo**</dt></span><span class="sxs-lookup"><span data-stu-id="10820-139"><dt>**Errors from the device**</dt></span></span> </dl>            | <span data-ttu-id="10820-140">Cualquier número de errores de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10820-140">Any of a number of device errors.</span></span><br/>                                  |
| <dl> <span data-ttu-id="10820-141"><dt>**Errores del cliente DRM**</dt></span><span class="sxs-lookup"><span data-stu-id="10820-141"><dt>**Errors from the DRM Client**</dt></span></span> </dl>        | <span data-ttu-id="10820-142">Cualquiera de los errores internos del cliente DRM.</span><span class="sxs-lookup"><span data-stu-id="10820-142">Any of a number of internal DRM client errors.</span></span><br/>                     |
| <dl> <span data-ttu-id="10820-143"><dt>**dispositivo \_ E \_ dispositivo \_ no \_ WMDRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="10820-143"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl> | <span data-ttu-id="10820-144">El dispositivo especificado no es un dispositivo compatible con DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="10820-144">The specified device is not a Windows Media DRM compatible device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="10820-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10820-145">Remarks</span></span>

<span data-ttu-id="10820-146">Antes de llamar a este método, la aplicación debe llamar a [**IWMDRMDeviceApp:: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) o [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) para comprobar que todos los componentes de DRM del dispositivo están actualizados.</span><span class="sxs-lookup"><span data-stu-id="10820-146">Before calling this method, the application should call [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) to verify that all the device's DRM components are up to date.</span></span> <span data-ttu-id="10820-147">Solo se puede llamar a este método en un dispositivo que admita Windows Media DRM 10 para dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="10820-147">This method can only be called on a device that supports Windows Media DRM 10 for Portable Devices.</span></span>

<span data-ttu-id="10820-148">Los *pbstrMeterData* de datos recuperados deben enviarse a la dirección URL especificada por *pbstrMeterURL*.</span><span class="sxs-lookup"><span data-stu-id="10820-148">The retrieved data *pbstrMeterData* should be sent to the URL specified by *pbstrMeterURL*.</span></span> <span data-ttu-id="10820-149">Asegúrese de codificar en URL los datos recuperados para que no se modifiquen durante la transferencia.</span><span class="sxs-lookup"><span data-stu-id="10820-149">Be sure to URL-encode the retrieved data so that it does not get modified during transfer.</span></span>

<span data-ttu-id="10820-150">Consulte [control del contenido protegido en la aplicación](handling-protected-content-in-the-application.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="10820-150">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="examples"></a><span data-ttu-id="10820-151">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="10820-151">Examples</span></span>

<span data-ttu-id="10820-152">En el siguiente ejemplo de código de C++ se crea un objeto **WMDRMDeviceApp** , se comprueba que el dispositivo es un dispositivo DRM 10 de Windows Media, que su reloj es preciso y, a continuación, solicita los datos de medición.</span><span class="sxs-lookup"><span data-stu-id="10820-152">The following C++ code example creates a **WMDRMDeviceApp** object, verifies that the device is a Windows Media DRM 10 device, that its clock is accurate, and then requests the metering data.</span></span>


```C++
HRESULT hr = S_OK;
// Create the WMDRMDeviceApp object.
CComPtr<IWMDRMDeviceApp> pDRM;
hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

// Find out first if the device is a WMDRM 10 device, and if it requires
// any clock updates.
DWORD status = 0;
hr = pDRM->QueryDeviceStatus(pDevice, &status);

if (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. Nothing can be updated,
    return E_FAIL;                   // and metering cannot be performed.
else if (status & WMDRM_DEVICE_REVOKED) // Device is revoked.
    return E_FAIL;
else if (status & WMDRM_DEVICE_NEEDCLOCK || 
    status & WMDRM_CLIENT_NEEDINDIV ||
    status & WMDRM_DEVICE_REFRESHCLOCK)
{
    // Need to update device clock. 
    // Using custom function, which is synchronous.
    hr = myAcquireDeviceData(pDRM, pDevice, this, status, &result);
    if (hr != S_OK || result != 0)    // Couldn't perform the updates.
        return E_FAIL;    
}

// Any updates have been performed. Now get the metering information from the device.
CComBSTR meterCert(METERCERT);
CComBSTR URL;
CComBSTR rawdata;
CComBSTR data;
hr = pDRM->GenerateMeterChallenge(pDevice, meterCert, &URL, &rawdata);
if (hr == S_OK)
    ..... Send to URL...
```



## <a name="requirements"></a><span data-ttu-id="10820-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10820-153">Requirements</span></span>



| <span data-ttu-id="10820-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="10820-154">Requirement</span></span> | <span data-ttu-id="10820-155">Value</span><span class="sxs-lookup"><span data-stu-id="10820-155">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10820-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10820-156">Header</span></span><br/>  | <dl> <span data-ttu-id="10820-157"><dt>WMDRMDeviceApp. h (también requiere Wmdrmdeviceapp \_ i, generado a partir de WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="10820-157"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="10820-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="10820-158">Library</span></span><br/> | <dl> <span data-ttu-id="10820-159"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10820-159"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="10820-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="10820-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10820-161">**Control del contenido protegido en la aplicación**</span><span class="sxs-lookup"><span data-stu-id="10820-161">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="10820-162">**Interfaz IWMDMDevice**</span><span class="sxs-lookup"><span data-stu-id="10820-162">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="10820-163">**Interfaz IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="10820-163">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





