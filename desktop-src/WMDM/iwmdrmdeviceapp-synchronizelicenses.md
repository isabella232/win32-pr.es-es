---
title: Método IWMDRMDeviceApp SynchronizeLicenses (WMDRMDeviceApp. h)
description: El método SynchronizeLicenses actualiza las licencias en un dispositivo cuando están a la expiración.
ms.assetid: 352378c1-7432-476c-98e9-d811165c020e
keywords:
- Método SynchronizeLicenses de Windows Media Administrador de dispositivos
- Método SynchronizeLicenses de Windows Media Administrador de dispositivos, interfaz IWMDRMDeviceApp
- Interfaz IWMDRMDeviceApp de Windows Media Administrador de dispositivos, método SynchronizeLicenses
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.SynchronizeLicenses
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b08f3457fec55a0eb519419feddf4594a2cbfac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699803"
---
# <a name="iwmdrmdeviceappsynchronizelicenses-method"></a><span data-ttu-id="9d4d7-106">IWMDRMDeviceApp:: SynchronizeLicenses (método)</span><span class="sxs-lookup"><span data-stu-id="9d4d7-106">IWMDRMDeviceApp::SynchronizeLicenses method</span></span>

<span data-ttu-id="9d4d7-107">El método **SynchronizeLicenses** actualiza las licencias en un dispositivo cuando están a la expiración.</span><span class="sxs-lookup"><span data-stu-id="9d4d7-107">The **SynchronizeLicenses** method updates licenses on a device when they are close to expiring.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d4d7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d4d7-108">Syntax</span></span>


```C++
HRESULT SynchronizeLicenses(
  [in] IWMDMDevice    *pDevice,
  [in] IWMDMProgress3 *pProgressCallback,
  [in] DWORD          cMinCountThreshold,
  [in] DWORD          cMinHoursThreshold
);
```



## <a name="parameters"></a><span data-ttu-id="9d4d7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d4d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d4d7-110">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d4d7-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d4d7-111">Puntero a un objeto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="9d4d7-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="9d4d7-112">*pProgressCallback* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d4d7-112">*pProgressCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d4d7-113">Devolución de llamada de progreso que recibirá el progreso de los pasos que pueda necesitar llevar a cabo. El paso se identifica mediante el parámetro *EventID* del método [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) denominado.</span><span class="sxs-lookup"><span data-stu-id="9d4d7-113">Progress callback that will receive progress of any steps that it might need to carry out. The step is identified by the *EventId* parameter of the [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) method called.</span></span>

</dd> <dt>

<span data-ttu-id="9d4d7-114">*cMinCountThreshold* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d4d7-114">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d4d7-115">Número mínimo opcional de recuento de reproducción restante en una licencia de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9d4d7-115">Optional minimum remaining play count on a device license.</span></span>

</dd> <dt>

<span data-ttu-id="9d4d7-116">*cMinHoursThreshold* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d4d7-116">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d4d7-117">Número mínimo opcional de horas restantes en una licencia de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9d4d7-117">Optional minimum remaining hours on a device license.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d4d7-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d4d7-118">Return value</span></span>

<span data-ttu-id="9d4d7-119">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9d4d7-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9d4d7-120">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="9d4d7-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9d4d7-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9d4d7-121">Return code</span></span>                                                                                                         | <span data-ttu-id="9d4d7-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d4d7-122">Description</span></span>                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9d4d7-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9d4d7-123"><dt>**S\_OK**</dt></span></span> </dl>                                | <span data-ttu-id="9d4d7-124">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="9d4d7-124">The method succeeded.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="9d4d7-125"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9d4d7-125"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                   | <span data-ttu-id="9d4d7-126">Uno o varios argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="9d4d7-126">One or more arguments are not valid.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="9d4d7-127"><dt>**DRM \_ E \_ INVALIDXMLTAG**</dt></span><span class="sxs-lookup"><span data-stu-id="9d4d7-127"><dt>**DRM\_E\_INVALIDXMLTAG**</dt></span></span> </dl>                | <span data-ttu-id="9d4d7-128">XML tiene un formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="9d4d7-128">XML is improperly formed.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="9d4d7-129"><dt>**DRM \_ E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="9d4d7-129"><dt>**DRM\_E\_NOTIMPL**</dt></span></span> </dl>                      | <span data-ttu-id="9d4d7-130">Esta funcionalidad no está implementada actualmente.</span><span class="sxs-lookup"><span data-stu-id="9d4d7-130">This functionality is not currently implemented.</span></span> <span data-ttu-id="9d4d7-131">(SyncLicenses w/ *pDevice* = null)</span><span class="sxs-lookup"><span data-stu-id="9d4d7-131">(SyncLicenses w/ *pDevice* =NULL)</span></span><br/>                                                               |
| <dl> <span data-ttu-id="9d4d7-132"><dt>**DRM \_ E \_ NOXMLCLOSETAG**</dt></span><span class="sxs-lookup"><span data-stu-id="9d4d7-132"><dt>**DRM\_E\_NOXMLCLOSETAG**</dt></span></span> </dl>                | <span data-ttu-id="9d4d7-133">El XML de la licencia tenía un formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="9d4d7-133">The license XML was improperly formed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="9d4d7-134"><dt>**DRM \_ E \_ NOXMLOPENTAG**</dt></span><span class="sxs-lookup"><span data-stu-id="9d4d7-134"><dt>**DRM\_E\_NOXMLOPENTAG**</dt></span></span> </dl>                 | <span data-ttu-id="9d4d7-135">El XML de la licencia tenía un formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="9d4d7-135">The license XML was improperly formed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="9d4d7-136"><dt>**DRM \_ E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9d4d7-136"><dt>**DRM\_E\_OUTOFMEMORY**</dt></span></span> </dl>                  | <span data-ttu-id="9d4d7-137">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="9d4d7-137">Out of memory.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="9d4d7-138"><dt>**DRM \_ E \_ XMLNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="9d4d7-138"><dt>**DRM\_E\_XMLNOTFOUND**</dt></span></span> </dl>                  | <span data-ttu-id="9d4d7-139">No se pudo encontrar una etiqueta XML necesaria en la licencia.</span><span class="sxs-lookup"><span data-stu-id="9d4d7-139">Failed to find a required XML tag in the license.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="9d4d7-140"><dt>**dispositivo \_ E \_ dispositivo \_ no \_ WMDRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9d4d7-140"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl>    | <span data-ttu-id="9d4d7-141">El dispositivo especificado no es un dispositivo compatible con DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9d4d7-141">The specified device is not a Windows Media DRM-compatible device.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="9d4d7-142"><dt>**el \_ DRM de NS E \_ requiere la \_ \_ individualización**</dt></span><span class="sxs-lookup"><span data-stu-id="9d4d7-142"><dt>**NS\_E\_DRM\_NEEDS\_INDIVIDUALIZATION**</dt></span></span> </dl> | <span data-ttu-id="9d4d7-143">DRM requiere un cuadro negro individual para realizar esta función.</span><span class="sxs-lookup"><span data-stu-id="9d4d7-143">The DRM requires an individualized black box to perform this function.</span></span> <span data-ttu-id="9d4d7-144">En otras palabras, el SDK de Windows Media Format requiere una actualización de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9d4d7-144">In other words, the Windows Media Format SDK requires a security upgrade.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9d4d7-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9d4d7-145">Remarks</span></span>

<span data-ttu-id="9d4d7-146">Esta llamada solo se puede realizar en un dispositivo que admita Windows Media DRM 10 para dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="9d4d7-146">This call can only be made on a device that supports Windows Media DRM 10 for Portable Devices.</span></span> <span data-ttu-id="9d4d7-147">Debe especificar al menos un parámetro de umbral.</span><span class="sxs-lookup"><span data-stu-id="9d4d7-147">You must specify at least one threshold parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d4d7-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d4d7-148">Requirements</span></span>



| <span data-ttu-id="9d4d7-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d4d7-149">Requirement</span></span> | <span data-ttu-id="9d4d7-150">Value</span><span class="sxs-lookup"><span data-stu-id="9d4d7-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4d7-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d4d7-151">Header</span></span><br/>  | <dl> <span data-ttu-id="9d4d7-152"><dt>WMDRMDeviceApp. h (también requiere Wmdrmdeviceapp \_ i, generado a partir de WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="9d4d7-152"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="9d4d7-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9d4d7-153">Library</span></span><br/> | <dl> <span data-ttu-id="9d4d7-154"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d4d7-154"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="9d4d7-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d4d7-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d4d7-156">**Control del contenido protegido en la aplicación**</span><span class="sxs-lookup"><span data-stu-id="9d4d7-156">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="9d4d7-157">**Interfaz IWMDMProgress3**</span><span class="sxs-lookup"><span data-stu-id="9d4d7-157">**IWMDMProgress3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[<span data-ttu-id="9d4d7-158">**Interfaz IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="9d4d7-158">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





