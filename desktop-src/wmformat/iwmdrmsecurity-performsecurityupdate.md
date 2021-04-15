---
title: Método IWMDRMSecurity PerformSecurityUpdate (wmdrmsdk. h)
description: El método PerformSecurityUpdate inicia una actualización de seguridad para el subsistema DRM en el equipo local.
ms.assetid: e450a1e3-6024-4c00-9978-fbc88fde2101
keywords:
- Método PerformSecurityUpdate formato de Windows Media
- Método PerformSecurityUpdate formato de Windows Media, interfaz IWMDRMSecurity
- Interfaz IWMDRMSecurity formato de Windows Media, método PerformSecurityUpdate
topic_type:
- apiref
api_name:
- IWMDRMSecurity.PerformSecurityUpdate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34a1e92edd279655737a2e8f3b7ce4e77e27fd5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708263"
---
# <a name="iwmdrmsecurityperformsecurityupdate-method"></a><span data-ttu-id="996b0-106">IWMDRMSecurity::P método erformSecurityUpdate</span><span class="sxs-lookup"><span data-stu-id="996b0-106">IWMDRMSecurity::PerformSecurityUpdate method</span></span>

<span data-ttu-id="996b0-107">El método **PerformSecurityUpdate** inicia una actualización de seguridad para el subsistema DRM en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="996b0-107">The **PerformSecurityUpdate** method initiates a security update to the DRM subsystem on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="996b0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="996b0-108">Syntax</span></span>


```C++
HRESULT PerformSecurityUpdate(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="996b0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="996b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="996b0-110">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="996b0-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="996b0-111">Opción de actualización expresada como una de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="996b0-111">Update option expressed as one of the following flags.</span></span>



| <span data-ttu-id="996b0-112">Marca</span><span class="sxs-lookup"><span data-stu-id="996b0-112">Flag</span></span>                                          | <span data-ttu-id="996b0-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="996b0-113">Description</span></span>                                                                                     |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="996b0-114">la \_ seguridad de WMDRM \_ realiza \_ indiv</span><span class="sxs-lookup"><span data-stu-id="996b0-114">WMDRM\_SECURITY\_PERFORM\_INDIV</span></span>               | <span data-ttu-id="996b0-115">Hace que el componente DRM se sutaque solo si la versión del cliente no está actualizada.</span><span class="sxs-lookup"><span data-stu-id="996b0-115">Causes the DRM component to be individualized only if the version of the client is out of date.</span></span> |
| <span data-ttu-id="996b0-116">\_actualización de \_ la \_ revocación \_ de seguridad de WMDRM</span><span class="sxs-lookup"><span data-stu-id="996b0-116">WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH</span></span> | <span data-ttu-id="996b0-117">Hace que se actualicen las listas de revocación en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="996b0-117">Causes the revocation lists on the client computer to be updated.</span></span>                               |
| <span data-ttu-id="996b0-118">seguridad de WMDRM, \_ \_ \_ forzar \_ indiv</span><span class="sxs-lookup"><span data-stu-id="996b0-118">WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV</span></span>        | <span data-ttu-id="996b0-119">Hace que el componente DRM se Suscríbase incluso si la versión del cliente está actualizada.</span><span class="sxs-lookup"><span data-stu-id="996b0-119">Causes the DRM component to be individualized even if the version of the client is up to date.</span></span>  |



 

</dd> <dt>

<span data-ttu-id="996b0-120">*ppunkCancelationCookie* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="996b0-120">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="996b0-121">Dirección de una variable que recibe un puntero a un objeto que se puede usar para cancelar esta operación.</span><span class="sxs-lookup"><span data-stu-id="996b0-121">Address of a variable that receives a pointer to an object that can be used to cancel this operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="996b0-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="996b0-122">Return value</span></span>

<span data-ttu-id="996b0-123">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="996b0-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="996b0-124">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="996b0-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="996b0-125">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="996b0-125">Return code</span></span>                                                                          | <span data-ttu-id="996b0-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="996b0-126">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="996b0-127"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="996b0-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="996b0-128">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="996b0-128">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="996b0-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="996b0-129">Remarks</span></span>

<span data-ttu-id="996b0-130">Este método se ejecuta de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="996b0-130">This method executes asynchronously.</span></span> <span data-ttu-id="996b0-131">Vuelve inmediatamente después de llamarse a y, a continuación, genera eventos en función de la marca establecida en el parámetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="996b0-131">It returns immediately after being called and then generates events depending on the flag set in the *dwFlags* parameter.</span></span>

<span data-ttu-id="996b0-132">En el caso de la individualización (la marca establecida en seguridad de WMDRM \_ \_ realiza \_ indiv o WMDRM \_ Security \_ realice \_ Force \_ indiv), se genera una serie de eventos **MEWMDRMIndividualizationProgress** seguidos de un evento **MEWMDRMIndividualizationCompleted** cuando se completa el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="996b0-132">For individualization (flag set to WMDRM\_SECURITY\_PERFORM\_INDIV or WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV), a series of **MEWMDRMIndividualizationProgress** events is generated followed by an **MEWMDRMIndividualizationCompleted** event when processing is complete.</span></span> <span data-ttu-id="996b0-133">El valor de cada uno de los eventos **MEWMDRMIndividualizationProgress** obtenidos mediante la llamada a **IMFMediaEvent:: GetValue** es un puntero **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="996b0-133">The value of each of the **MEWMDRMIndividualizationProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="996b0-134">Puede llamar al método **QueryInterface** de la interfaz **IUnknown** recuperada para obtener una instancia de la interfaz [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="996b0-134">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) interface.</span></span>

<span data-ttu-id="996b0-135">Para actualizar las listas de revocación (marca establecida en seguridad de WMDRM, \_ \_ realizar la actualización de \_ revocación \_ ), se genera un evento **MEWMDRMREvocationDownloadCompleted** cuando se completa el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="996b0-135">For refreshing the revocation lists (flag set to WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH), an **MEWMDRMREvocationDownloadCompleted** event is generated when processing is complete.</span></span>

> [!Note]  
> <span data-ttu-id="996b0-136">Cuando **PerformSecurityUpdate** complete la individualización, los únicos objetos existentes que reflejen el nuevo estado individualizado son los que heredan de **IWMDRMSecurity**.</span><span class="sxs-lookup"><span data-stu-id="996b0-136">When **PerformSecurityUpdate** completes individualization, the only existing objects that will reflect the new individualized state are those that inherit from **IWMDRMSecurity**.</span></span> <span data-ttu-id="996b0-137">No se actualizarán todos los demás objetos existentes.</span><span class="sxs-lookup"><span data-stu-id="996b0-137">All other existing objects will not be updated.</span></span> <span data-ttu-id="996b0-138">Debe liberar y volver a crear los demás objetos para que reflejen el nuevo estado de forma individual.</span><span class="sxs-lookup"><span data-stu-id="996b0-138">You must release and re-create any other objects so that they will reflect the new individualized state.</span></span>

 

<span data-ttu-id="996b0-139">Para obtener más información sobre el uso de los métodos asincrónicos de las API extendidas del cliente DRM de Windows Media, vea [usar el modelo de eventos de Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="996b0-139">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="996b0-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="996b0-140">Requirements</span></span>



| <span data-ttu-id="996b0-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="996b0-141">Requirement</span></span> | <span data-ttu-id="996b0-142">Value</span><span class="sxs-lookup"><span data-stu-id="996b0-142">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="996b0-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="996b0-143">Header</span></span><br/>  | <dl> <span data-ttu-id="996b0-144"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="996b0-144"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="996b0-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="996b0-145">Library</span></span><br/> | <dl> <span data-ttu-id="996b0-146"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="996b0-146"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="996b0-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="996b0-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="996b0-148">**Revocación y renovación de componentes automatizados**</span><span class="sxs-lookup"><span data-stu-id="996b0-148">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="996b0-149">**Ejemplo de individualización de DRM**</span><span class="sxs-lookup"><span data-stu-id="996b0-149">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="996b0-150">**Interfaz IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="996b0-150">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="996b0-151">**Realización de una individualización DRM**</span><span class="sxs-lookup"><span data-stu-id="996b0-151">**Performing DRM Individualization**</span></span>](performing-drm-individualization.md)
</dt> </dl>

 

 





