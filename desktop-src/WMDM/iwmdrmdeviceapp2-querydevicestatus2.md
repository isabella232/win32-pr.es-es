---
title: Método IWMDRMDeviceApp2 QueryDeviceStatus2 (WMDRMDeviceApp. h)
description: El método QueryDeviceStatus2 consulta un dispositivo para una funcionalidad o un estado DRM específico.
ms.assetid: f7e95fb7-5929-4a70-8580-a443e152e6d1
keywords:
- Método QueryDeviceStatus2 de Windows Media Administrador de dispositivos
- Método QueryDeviceStatus2 de Windows Media Administrador de dispositivos, interfaz IWMDRMDeviceApp2
- Interfaz IWMDRMDeviceApp2 de Windows Media Administrador de dispositivos, método QueryDeviceStatus2
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2.QueryDeviceStatus2
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338d1f03f8d1e63086bb260c9854c7dcf3e88514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699802"
---
# <a name="iwmdrmdeviceapp2querydevicestatus2-method"></a><span data-ttu-id="0ff28-106">IWMDRMDeviceApp2:: QueryDeviceStatus2 (método)</span><span class="sxs-lookup"><span data-stu-id="0ff28-106">IWMDRMDeviceApp2::QueryDeviceStatus2 method</span></span>

<span data-ttu-id="0ff28-107">El método **QueryDeviceStatus2** consulta un dispositivo para una funcionalidad o un estado DRM específico.</span><span class="sxs-lookup"><span data-stu-id="0ff28-107">The **QueryDeviceStatus2** method queries a device for a specific DRM status or capability.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ff28-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ff28-108">Syntax</span></span>


```C++
HRESULT QueryDeviceStatus2(
  [in]  IWMDMDevice *pDevice,
  [in]  DWORD       dwFlags,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="0ff28-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ff28-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ff28-110">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0ff28-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ff28-111">Puntero a un objeto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="0ff28-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="0ff28-112">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0ff28-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ff28-113">Uno o varios de los siguientes valores **DWORD** que especifican las funciones que se van a solicitar, combinadas con **una operación OR** bit a bit.</span><span class="sxs-lookup"><span data-stu-id="0ff28-113">One or more of the following **DWORD** values specifying which capabilities to request, combined with a bitwise **OR**.</span></span>



| <span data-ttu-id="0ff28-114">Marca</span><span class="sxs-lookup"><span data-stu-id="0ff28-114">Flag</span></span>                              | <span data-ttu-id="0ff28-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ff28-115">Description</span></span>                                                                  |
|-----------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0ff28-116">\_INDIVSTATUS de \_ cliente de consulta WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="0ff28-116">WMDRM\_QUERY\_CLIENT\_INDIVSTATUS</span></span> | <span data-ttu-id="0ff28-117">Consulte si los componentes DRM del equipo deben ser individualizados.</span><span class="sxs-lookup"><span data-stu-id="0ff28-117">Query whether the computer's DRM components need to be individualized.</span></span>       |
| <span data-ttu-id="0ff28-118">\_dispositivo de consulta WMDRM \_ \_ CLOCKSTATUS</span><span class="sxs-lookup"><span data-stu-id="0ff28-118">WMDRM\_QUERY\_DEVICE\_CLOCKSTATUS</span></span> | <span data-ttu-id="0ff28-119">Consulte si es necesario agregar o actualizar el reloj seguro del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ff28-119">Query whether the device's secure clock needs to be added or updated.</span></span>        |
| <span data-ttu-id="0ff28-120">\_dispositivo de consulta WMDRM \_ \_ ISREVOKED</span><span class="sxs-lookup"><span data-stu-id="0ff28-120">WMDRM\_QUERY\_DEVICE\_ISREVOKED</span></span>   | <span data-ttu-id="0ff28-121">Consulta si el dispositivo se ha revocado.</span><span class="sxs-lookup"><span data-stu-id="0ff28-121">Query whether the device is revoked.</span></span>                                         |
| <span data-ttu-id="0ff28-122">\_dispositivo de consulta WMDRM \_ \_ ISWMDRM</span><span class="sxs-lookup"><span data-stu-id="0ff28-122">WMDRM\_QUERY\_DEVICE\_ISWMDRM</span></span>     | <span data-ttu-id="0ff28-123">Consulta si el dispositivo admite Windows Media DRM 10 para dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="0ff28-123">Query whether the device supports Windows Media DRM 10 for Portable Devices.</span></span> |



 

</dd> <dt>

<span data-ttu-id="0ff28-124">*pdwStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0ff28-124">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ff28-125">Cero o más de los siguientes valores **DWORD** que especifican el estado de dispositivo solicitado, combinado con una operación **OR bit a** bit.</span><span class="sxs-lookup"><span data-stu-id="0ff28-125">Zero or more of the following **DWORD** values specifying the requested device status, combined with a bitwise **OR**.</span></span>



| <span data-ttu-id="0ff28-126">Status</span><span class="sxs-lookup"><span data-stu-id="0ff28-126">Status</span></span>                      | <span data-ttu-id="0ff28-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ff28-127">Description</span></span>                                              |
|-----------------------------|----------------------------------------------------------|
| <span data-ttu-id="0ff28-128">\_dispositivo \_ ISWMDRM de WMDRM</span><span class="sxs-lookup"><span data-stu-id="0ff28-128">WMDRM\_DEVICE\_ISWMDRM</span></span>      | <span data-ttu-id="0ff28-129">El dispositivo es compatible con DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0ff28-129">The device supports Windows Media DRM.</span></span>                   |
| <span data-ttu-id="0ff28-130">\_dispositivo \_ NEEDCLOCK de WMDRM</span><span class="sxs-lookup"><span data-stu-id="0ff28-130">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="0ff28-131">El dispositivo no tiene un reloj seguro.</span><span class="sxs-lookup"><span data-stu-id="0ff28-131">The device does not have a secure clock.</span></span>                 |
| <span data-ttu-id="0ff28-132">\_dispositivo WMDRM \_ revocado</span><span class="sxs-lookup"><span data-stu-id="0ff28-132">WMDRM\_DEVICE\_REVOKED</span></span>      | <span data-ttu-id="0ff28-133">El dispositivo se ha revocado.</span><span class="sxs-lookup"><span data-stu-id="0ff28-133">The device has been revoked.</span></span>                             |
| <span data-ttu-id="0ff28-134">\_NEEDINDIV de cliente WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="0ff28-134">WMDRM\_CLIENT\_NEEDINDIV</span></span>    | <span data-ttu-id="0ff28-135">Los componentes de DRM del equipo deben ser individualizados.</span><span class="sxs-lookup"><span data-stu-id="0ff28-135">The computer's DRM components need to be individualized.</span></span> |
| <span data-ttu-id="0ff28-136">\_dispositivo \_ REFRESHCLOCK de WMDRM</span><span class="sxs-lookup"><span data-stu-id="0ff28-136">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="0ff28-137">El reloj debe actualizarse.</span><span class="sxs-lookup"><span data-stu-id="0ff28-137">The clock needs to be refreshed.</span></span>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ff28-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ff28-138">Return value</span></span>

<span data-ttu-id="0ff28-139">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0ff28-139">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0ff28-140">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="0ff28-140">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0ff28-141">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0ff28-141">Return code</span></span>                                                                                                              | <span data-ttu-id="0ff28-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ff28-142">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ff28-143"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0ff28-143"><dt>**S\_OK**</dt></span></span> </dl>                                     | <span data-ttu-id="0ff28-144">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="0ff28-144">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="0ff28-145"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0ff28-145"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                        | <span data-ttu-id="0ff28-146">Uno o varios argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="0ff28-146">One or more arguments are not valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="0ff28-147"><dt>**\_ \_ \_ certificado no válido de DRM E DRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0ff28-147"><dt>**NS\_E\_DRM\_INVALID\_CERTIFICATE**</dt></span></span> </dl>          | <span data-ttu-id="0ff28-148">El certificado de dispositivo recuperado del dispositivo no es válido.</span><span class="sxs-lookup"><span data-stu-id="0ff28-148">The device certificate retrieved from the device is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="0ff28-149"><dt>**\_DRM E \_ DRM \_ no \_ puede \_ obtener \_ el \_ certificado del dispositivo**</dt></span><span class="sxs-lookup"><span data-stu-id="0ff28-149"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_DEVICE\_CERT**</dt></span></span> </dl> | <span data-ttu-id="0ff28-150">No se pudo recuperar el certificado de dispositivo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ff28-150">Failed to retrieve the device certificate from the device.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="0ff28-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ff28-151">Remarks</span></span>

<span data-ttu-id="0ff28-152">Se debe llamar a este método antes de realizar cualquier acción restringida en el contenido DRM, como transferir contenido DRM al dispositivo o adquirir información de medición.</span><span class="sxs-lookup"><span data-stu-id="0ff28-152">This method should be called before performing any restricted actions on DRM content, such as transferring DRM content to the device, or acquiring metering information.</span></span> <span data-ttu-id="0ff28-153">Si los valores recuperados por *pdwStatus* indican que es necesario realizar alguna acción (por ejemplo, la individualización del escritorio o la adquisición de un reloj para el dispositivo), la aplicación debe llamar a [**IWMDRMDeviceApp:: AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) y pasar el valor de *pdwStatus* recuperado de esta función al parámetro *dwFlags* en **AcquireDeviceData**.</span><span class="sxs-lookup"><span data-stu-id="0ff28-153">If the values retrieved by *pdwStatus* indicate that some action needs to be performed (such as individualization for the desktop or acquiring a clock for the device), the application should call [**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) and pass in the retrieved *pdwStatus* value from this function to the *dwFlags* parameter in **AcquireDeviceData**.</span></span> <span data-ttu-id="0ff28-154">Si se devuelve cero, el dispositivo no admite Windows Media DRM 10 para dispositivos portátiles y no es necesario realizar ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="0ff28-154">If zero is returned, the device does not support Windows Media DRM 10 for Portable Devices, and no actions need be taken.</span></span> <span data-ttu-id="0ff28-155">Consulte [control del contenido protegido en la aplicación](handling-protected-content-in-the-application.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="0ff28-155">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ff28-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ff28-156">Requirements</span></span>



| <span data-ttu-id="0ff28-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ff28-157">Requirement</span></span> | <span data-ttu-id="0ff28-158">Value</span><span class="sxs-lookup"><span data-stu-id="0ff28-158">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ff28-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ff28-159">Header</span></span><br/>  | <dl> <span data-ttu-id="0ff28-160"><dt>WMDRMDeviceApp. h (también requiere Wmdrmdeviceapp \_ i, generado a partir de WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="0ff28-160"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="0ff28-161">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0ff28-161">Library</span></span><br/> | <dl> <span data-ttu-id="0ff28-162"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ff28-162"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="0ff28-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ff28-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ff28-164">**Control del contenido protegido en la aplicación**</span><span class="sxs-lookup"><span data-stu-id="0ff28-164">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="0ff28-165">**IWMDRMDeviceApp::QueryDeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="0ff28-165">**IWMDRMDeviceApp::QueryDeviceStatus**</span></span>](iwmdrmdeviceapp-querydevicestatus.md)
</dt> <dt>

[<span data-ttu-id="0ff28-166">**Interfaz IWMDRMDeviceApp2**</span><span class="sxs-lookup"><span data-stu-id="0ff28-166">**IWMDRMDeviceApp2 Interface**</span></span>](iwmdrmdeviceapp2.md)
</dt> </dl>

 

 





