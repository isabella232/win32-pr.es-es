---
title: Método IWMDRMDeviceApp QueryDeviceStatus (WMDRMDeviceApp. h)
description: El método QueryDeviceStatus consulta el estado y las capacidades actuales de DRM de un dispositivo.
ms.assetid: cd5a75d5-d7f8-4077-a9fc-6e7ddd7c796b
keywords:
- Método QueryDeviceStatus de Windows Media Administrador de dispositivos
- Método QueryDeviceStatus de Windows Media Administrador de dispositivos, interfaz IWMDRMDeviceApp
- Interfaz IWMDRMDeviceApp de Windows Media Administrador de dispositivos, método QueryDeviceStatus
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.QueryDeviceStatus
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e0f4fad5ff9026ce70fc21712506eb4796d76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699679"
---
# <a name="iwmdrmdeviceappquerydevicestatus-method"></a><span data-ttu-id="1f18f-106">IWMDRMDeviceApp:: QueryDeviceStatus (método)</span><span class="sxs-lookup"><span data-stu-id="1f18f-106">IWMDRMDeviceApp::QueryDeviceStatus method</span></span>

<span data-ttu-id="1f18f-107">El método **QueryDeviceStatus** consulta el estado y las capacidades actuales de DRM de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1f18f-107">The **QueryDeviceStatus** method queries a device for its current DRM status and capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f18f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f18f-108">Syntax</span></span>


```C++
HRESULT QueryDeviceStatus(
  [in]  IWMDMDevice *pDevice,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="1f18f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f18f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f18f-110">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1f18f-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f18f-111">Puntero a un objeto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="1f18f-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="1f18f-112">*pdwStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1f18f-112">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f18f-113">Cero o más de los siguientes valores **DWORD** que describen los aspectos DRM del dispositivo, combinados con **una operación OR** bit a bit.</span><span class="sxs-lookup"><span data-stu-id="1f18f-113">Zero or more of the following **DWORD** values describing the DRM aspects of the device, combined with a bitwise **OR**.</span></span> <span data-ttu-id="1f18f-114">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="1f18f-114">See Remarks.</span></span>



| <span data-ttu-id="1f18f-115">Status</span><span class="sxs-lookup"><span data-stu-id="1f18f-115">Status</span></span>                      | <span data-ttu-id="1f18f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f18f-116">Description</span></span>                                  |
|-----------------------------|----------------------------------------------|
| <span data-ttu-id="1f18f-117">\_dispositivo \_ ISWMDRM de WMDRM</span><span class="sxs-lookup"><span data-stu-id="1f18f-117">WMDRM\_DEVICE\_ISWMDRM</span></span>      | <span data-ttu-id="1f18f-118">El dispositivo es compatible con DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1f18f-118">The device supports Windows Media DRM.</span></span>       |
| <span data-ttu-id="1f18f-119">\_dispositivo \_ NEEDCLOCK de WMDRM</span><span class="sxs-lookup"><span data-stu-id="1f18f-119">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="1f18f-120">El dispositivo no tiene un reloj seguro.</span><span class="sxs-lookup"><span data-stu-id="1f18f-120">The device does not have a secure clock.</span></span>     |
| <span data-ttu-id="1f18f-121">\_dispositivo WMDRM \_ revocado</span><span class="sxs-lookup"><span data-stu-id="1f18f-121">WMDRM\_DEVICE\_REVOKED</span></span>      | <span data-ttu-id="1f18f-122">El dispositivo se ha revocado.</span><span class="sxs-lookup"><span data-stu-id="1f18f-122">The device has been revoked.</span></span>                 |
| <span data-ttu-id="1f18f-123">\_NEEDINDIV de cliente WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="1f18f-123">WMDRM\_CLIENT\_NEEDINDIV</span></span>    | <span data-ttu-id="1f18f-124">La seguridad de DRM debe ser individualizada.</span><span class="sxs-lookup"><span data-stu-id="1f18f-124">The DRM security needs to be individualized.</span></span> |
| <span data-ttu-id="1f18f-125">\_dispositivo \_ REFRESHCLOCK de WMDRM</span><span class="sxs-lookup"><span data-stu-id="1f18f-125">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="1f18f-126">El reloj debe actualizarse.</span><span class="sxs-lookup"><span data-stu-id="1f18f-126">The clock needs to be refreshed.</span></span>             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f18f-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f18f-127">Return value</span></span>

<span data-ttu-id="1f18f-128">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1f18f-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1f18f-129">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="1f18f-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1f18f-130">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1f18f-130">Return code</span></span>                                                                                                              | <span data-ttu-id="1f18f-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f18f-131">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1f18f-132"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1f18f-132"><dt>**S\_OK**</dt></span></span> </dl>                                     | <span data-ttu-id="1f18f-133">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="1f18f-133">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="1f18f-134"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1f18f-134"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                        | <span data-ttu-id="1f18f-135">El argumento de entrada no es válido.</span><span class="sxs-lookup"><span data-stu-id="1f18f-135">The input argument is not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="1f18f-136"><dt>**\_ \_ \_ certificado no válido de DRM E DRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f18f-136"><dt>**NS\_E\_DRM\_INVALID\_CERTIFICATE**</dt></span></span> </dl>          | <span data-ttu-id="1f18f-137">El certificado de dispositivo recuperado del dispositivo no es válido.</span><span class="sxs-lookup"><span data-stu-id="1f18f-137">The device certificate retrieved from the device is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="1f18f-138"><dt>**\_DRM E \_ DRM \_ no \_ puede \_ obtener \_ el \_ certificado del dispositivo**</dt></span><span class="sxs-lookup"><span data-stu-id="1f18f-138"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_DEVICE\_CERT**</dt></span></span> </dl> | <span data-ttu-id="1f18f-139">No se pudo recuperar el certificado de dispositivo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1f18f-139">Failed to retrieve the device certificate from the device.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="1f18f-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f18f-140">Remarks</span></span>

<span data-ttu-id="1f18f-141">Se debe llamar a este método antes de realizar cualquier acción restringida en el contenido DRM, como transferir contenido DRM al dispositivo o adquirir información de medición.</span><span class="sxs-lookup"><span data-stu-id="1f18f-141">This method should be called before performing any restricted actions on DRM content, such as transferring DRM content to the device, or acquiring metering information.</span></span> <span data-ttu-id="1f18f-142">Si los valores recuperados por *pdwStatus* indican que es necesario realizar alguna acción (por ejemplo, la individualización del escritorio o la adquisición de un reloj para el dispositivo), la aplicación debe llamar a [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) y pasar el valor de *pdwStatus* recuperado de esta función al parámetro *dwFlags* en **AcquireDeviceData**.</span><span class="sxs-lookup"><span data-stu-id="1f18f-142">If the values retrieved by *pdwStatus* indicate that some action needs to be performed (such as individualization for the desktop or acquiring a clock for the device), the application should call [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) and pass the retrieved *pdwStatus* value from this function to the *dwFlags* parameter in **AcquireDeviceData**.</span></span> <span data-ttu-id="1f18f-143">Si se devuelve cero, el dispositivo no admite Windows Media DRM 10 para dispositivos portátiles y no es necesario realizar ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="1f18f-143">If zero is returned, the device does not support Windows Media DRM 10 for Portable Devices, and no actions need be taken.</span></span> <span data-ttu-id="1f18f-144">Consulte [control del contenido protegido en la aplicación](handling-protected-content-in-the-application.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="1f18f-144">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="examples"></a><span data-ttu-id="1f18f-145">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1f18f-145">Examples</span></span>

<span data-ttu-id="1f18f-146">En el siguiente ejemplo de código de C++ se crea un objeto **WMDRMDeviceApp** , se comprueba que el dispositivo es un dispositivo DRM 10 de Windows Media, que su reloj es preciso y, a continuación, solicita los datos de medición.</span><span class="sxs-lookup"><span data-stu-id="1f18f-146">The following C++ code example creates a **WMDRMDeviceApp** object, verifies that the device is a Windows Media DRM 10 device, that its clock is accurate, and then requests the metering data.</span></span>


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
```



## <a name="requirements"></a><span data-ttu-id="1f18f-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f18f-147">Requirements</span></span>



| <span data-ttu-id="1f18f-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f18f-148">Requirement</span></span> | <span data-ttu-id="1f18f-149">Value</span><span class="sxs-lookup"><span data-stu-id="1f18f-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f18f-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f18f-150">Header</span></span><br/>  | <dl> <span data-ttu-id="1f18f-151"><dt>WMDRMDeviceApp. h (también requiere Wmdrmdeviceapp \_ i, generado a partir de WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="1f18f-151"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="1f18f-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1f18f-152">Library</span></span><br/> | <dl> <span data-ttu-id="1f18f-153"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f18f-153"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="1f18f-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f18f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f18f-155">**Control del contenido protegido en la aplicación**</span><span class="sxs-lookup"><span data-stu-id="1f18f-155">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="1f18f-156">**Interfaz IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="1f18f-156">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> <dt>

[<span data-ttu-id="1f18f-157">**IWMDRMDeviceApp2::QueryDeviceStatus2**</span><span class="sxs-lookup"><span data-stu-id="1f18f-157">**IWMDRMDeviceApp2::QueryDeviceStatus2**</span></span>](iwmdrmdeviceapp2-querydevicestatus2.md)
</dt> </dl>

 

 





