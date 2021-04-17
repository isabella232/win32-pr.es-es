---
title: Método IWMDRMLicenseManagement CleanLicenseStore (wmdrmsdk. h)
description: El método CleanLicenseStore quita las licencias inutilizables del almacén de licencias temporal y desfragmenta el almacén de licencias local para mejorar el rendimiento.
ms.assetid: 07ddd6f8-a091-4c18-81d3-c4d0c6026b6b
keywords:
- Método CleanLicenseStore formato de Windows Media
- Método CleanLicenseStore formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método CleanLicenseStore
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CleanLicenseStore
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9327fd836cf742f5495c29767be93d914c0f187
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718674"
---
# <a name="iwmdrmlicensemanagementcleanlicensestore-method"></a><span data-ttu-id="607c2-106">IWMDRMLicenseManagement:: CleanLicenseStore (método)</span><span class="sxs-lookup"><span data-stu-id="607c2-106">IWMDRMLicenseManagement::CleanLicenseStore method</span></span>

<span data-ttu-id="607c2-107">El método **CleanLicenseStore** quita las licencias inutilizables del almacén de licencias temporal y desfragmenta el almacén de licencias local para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="607c2-107">The **CleanLicenseStore** method removes unusable licenses from the temporary license store and defragments the local license store to improve performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="607c2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="607c2-108">Syntax</span></span>


```C++
HRESULT CleanLicenseStore(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="607c2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="607c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="607c2-110">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="607c2-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="607c2-111">Marcas que especifican las opciones de limpieza del almacén de licencias que se van a utilizar.</span><span class="sxs-lookup"><span data-stu-id="607c2-111">Flags specifying the license store cleaning options to use.</span></span> <span data-ttu-id="607c2-112">Establezca en una de las constantes de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="607c2-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="607c2-113">Constante</span><span class="sxs-lookup"><span data-stu-id="607c2-113">Constant</span></span>                            | <span data-ttu-id="607c2-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="607c2-114">Description</span></span>                                                                                                                                                                    |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="607c2-115">\_sincronización del \_ almacén de licencias limpio \_ de WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="607c2-115">WMDRM\_CLEAN\_LICENSE\_STORE\_SYNC</span></span>  | <span data-ttu-id="607c2-116">La operación de limpieza se realizará sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="607c2-116">The clean operation will be performed synchronously.</span></span> <span data-ttu-id="607c2-117">Este método no devolverá ningún resultado hasta que se complete la operación.</span><span class="sxs-lookup"><span data-stu-id="607c2-117">This method will not return until the operation is complete.</span></span>                                                              |
| <span data-ttu-id="607c2-118">\_ \_ \_ almacenamiento asincrónico de licencias de WMDRM Clean \_</span><span class="sxs-lookup"><span data-stu-id="607c2-118">WMDRM\_CLEAN\_LICENSE\_STORE\_ASYNC</span></span> | <span data-ttu-id="607c2-119">La operación de limpieza se realizará de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="607c2-119">The clean operation will be performed asynchronously.</span></span> <span data-ttu-id="607c2-120">Este método devolverá inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="607c2-120">This method will return immediately.</span></span> <span data-ttu-id="607c2-121">Una vez completada la operación, se enviará el evento MELicenseStoreCleaned.</span><span class="sxs-lookup"><span data-stu-id="607c2-121">When the operation is complete, the media event MELicenseStoreCleaned will be sent.</span></span> |



 

</dd> <dt>

<span data-ttu-id="607c2-122">*ppunkCancelationCookie* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="607c2-122">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="607c2-123">Puntero que recibe un puntero a la interfaz **IUnknown** de un objeto que identifica esta llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="607c2-123">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="607c2-124">Este puntero de interfaz se puede usar para cancelar la llamada asincrónica llamando al método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="607c2-124">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="607c2-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="607c2-125">Return value</span></span>

<span data-ttu-id="607c2-126">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="607c2-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="607c2-127">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="607c2-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="607c2-128">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="607c2-128">Return code</span></span>                                                                                            | <span data-ttu-id="607c2-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="607c2-129">Description</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="607c2-130"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="607c2-130"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="607c2-131">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="607c2-131">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="607c2-132"><dt>**DRM \_ E \_ LICENSENOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="607c2-132"><dt>**DRM\_E\_LICENSENOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="607c2-133">No hay ningún almacén de licencias temporal en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="607c2-133">There is no temporary license store on the client computer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="607c2-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="607c2-134">Remarks</span></span>

<span data-ttu-id="607c2-135">Este método se ejecuta de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="607c2-135">This method executes asynchronously.</span></span> <span data-ttu-id="607c2-136">Vuelve inmediatamente después de llamarlo y, a continuación, genera un evento **MEWMDRMLicenseStoreCleaned** cuando se completa el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="607c2-136">It returns immediately after being called and then generates an **MEWMDRMLicenseStoreCleaned** event when processing is complete.</span></span>

<span data-ttu-id="607c2-137">Para obtener más información sobre el uso de los métodos asincrónicos de las API extendidas del cliente DRM de Windows Media, vea [usar el modelo de eventos de Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="607c2-137">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="607c2-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="607c2-138">Requirements</span></span>



| <span data-ttu-id="607c2-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="607c2-139">Requirement</span></span> | <span data-ttu-id="607c2-140">Value</span><span class="sxs-lookup"><span data-stu-id="607c2-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="607c2-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="607c2-141">Header</span></span><br/>  | <dl> <span data-ttu-id="607c2-142"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="607c2-142"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="607c2-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="607c2-143">Library</span></span><br/> | <dl> <span data-ttu-id="607c2-144"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="607c2-144"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="607c2-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="607c2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="607c2-146">**Interfaz IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="607c2-146">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





