---
title: Método AcquireLicense de IWMDRMLicenseManagement (wmdrmsdk. h)
description: El método AcquireLicense adquiere de forma asincrónica una licencia de una dirección URL especificada.
ms.assetid: 2e134f39-1f45-4d3a-b7c7-460aa0a250d0
keywords:
- Método AcquireLicense de Windows Media Format
- Método AcquireLicense formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método AcquireLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.AcquireLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 279a3d4d84617c4a4fa5454d1f39f6f78f0cf3fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708804"
---
# <a name="iwmdrmlicensemanagementacquirelicense-method"></a><span data-ttu-id="ef30a-106">IWMDRMLicenseManagement:: AcquireLicense (método)</span><span class="sxs-lookup"><span data-stu-id="ef30a-106">IWMDRMLicenseManagement::AcquireLicense method</span></span>

<span data-ttu-id="ef30a-107">El método **AcquireLicense** adquiere de forma asincrónica una licencia de una dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="ef30a-107">The **AcquireLicense** method asynchronously acquires a license from a specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef30a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef30a-108">Syntax</span></span>


```C++
HRESULT AcquireLicense(
  [in]  BSTR     bstrURL,
  [in]  BSTR     bstrHeaderData,
  [in]  BSTR     bstrActions,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="ef30a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef30a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef30a-110">*bstrURL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef30a-110">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef30a-111">Dirección URL del servidor de licencias del que se va a adquirir la licencia.</span><span class="sxs-lookup"><span data-stu-id="ef30a-111">URL of the license server from which to acquire the license.</span></span> <span data-ttu-id="ef30a-112">Pase **null** para que el método analice la dirección URL del encabezado de contenido.</span><span class="sxs-lookup"><span data-stu-id="ef30a-112">Pass **NULL** to have the method parse the URL from the content header.</span></span>

</dd> <dt>

<span data-ttu-id="ef30a-113">*bstrHeaderData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef30a-113">*bstrHeaderData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef30a-114">Encabezado de contenido que se va a pasar al servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="ef30a-114">Content header to be passed to the license server.</span></span> <span data-ttu-id="ef30a-115">Si *bstrURL* es **null**, el método analizará la dirección URL de este encabezado.</span><span class="sxs-lookup"><span data-stu-id="ef30a-115">If *bstrURL* is **NULL**, the method will parse the URL from this header.</span></span> <span data-ttu-id="ef30a-116">Si *dwFlags* se establece en \_ la licencia de adquisición de WMDRM Legacy no \_ \_ \_ Silent, establezca este valor en el identificador de clave en lugar del encabezado de contenido completo.</span><span class="sxs-lookup"><span data-stu-id="ef30a-116">If *dwFlags* is set to WMDRM\_ACQUIRE\_LICENSE\_LEGACY\_NONSILENT, set this value to the key ID instead of the entire content header.</span></span>

</dd> <dt>

<span data-ttu-id="ef30a-117">*bstrActions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef30a-117">*bstrActions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef30a-118">Cadena que contiene cero o más acciones para las que se va a solicitar permiso en la licencia.</span><span class="sxs-lookup"><span data-stu-id="ef30a-118">String containing zero or more actions for which to request permission in the license.</span></span> <span data-ttu-id="ef30a-119">La cadena debe tener el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="ef30a-119">The string must be formatted as follows:</span></span>

-   <span data-ttu-id="ef30a-120">Cada acción debe definirse dentro de un elemento ACTION.</span><span class="sxs-lookup"><span data-stu-id="ef30a-120">Each action must be defined within an ACTION element.</span></span> <span data-ttu-id="ef30a-121">Los datos del elemento son la cadena de acción.</span><span class="sxs-lookup"><span data-stu-id="ef30a-121">The data of the element is the action string.</span></span>
-   <span data-ttu-id="ef30a-122">Todos los elementos ACTION deben estar contenidos dentro de un elemento ACTIONLIST.</span><span class="sxs-lookup"><span data-stu-id="ef30a-122">All ACTION elements must be contained within an ACTIONLIST element.</span></span>

    <span data-ttu-id="ef30a-123">Por ejemplo, la cadena para solicitar una licencia para reproducir contenido tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="ef30a-123">For example, the string to request a license to play content is formatted like this:</span></span>

    ```C++
    <ACTIONLIST><ACTION></ACTION></ACTIONLIST>
    ```

    

</dd> <dt>

<span data-ttu-id="ef30a-124">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef30a-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef30a-125">Marcas de opciones de adquisición de licencias.</span><span class="sxs-lookup"><span data-stu-id="ef30a-125">License acquisition option flags.</span></span> <span data-ttu-id="ef30a-126">Establezca en una de las constantes de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ef30a-126">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="ef30a-127">Constante</span><span class="sxs-lookup"><span data-stu-id="ef30a-127">Constant</span></span>                                   | <span data-ttu-id="ef30a-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef30a-128">Description</span></span>                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef30a-129">la licencia de adquisición de WMDRM es \_ \_ \_ silenciosa</span><span class="sxs-lookup"><span data-stu-id="ef30a-129">WMDRM\_ACQUIRE\_LICENSE\_SILENT</span></span>            | <span data-ttu-id="ef30a-130">La licencia se emitirá directamente a través de Internet sin confirmación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="ef30a-130">The license will be issued directly over the Internet without any confirmation from the client application.</span></span>              |
| <span data-ttu-id="ef30a-131">la licencia de adquisición de WMDRM no es \_ \_ \_ silenciosa</span><span class="sxs-lookup"><span data-stu-id="ef30a-131">WMDRM\_ACQUIRE\_LICENSE\_NONSILENT</span></span>         | <span data-ttu-id="ef30a-132">El subsistema DRM creará una solicitud de licencia que se devolverá de forma asincrónica para publicarla en el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="ef30a-132">The DRM subsystem will create a license request which will be returned asynchronously for posting to the license server.</span></span> |
| <span data-ttu-id="ef30a-133">licencia de adquisición de WMDRM \_ \_ \_ HEREDAda no \_ silenciosa</span><span class="sxs-lookup"><span data-stu-id="ef30a-133">WMDRM\_ACQUIRE\_LICENSE\_LEGACY\_NONSILENT</span></span> | <span data-ttu-id="ef30a-134">Lo mismo que la licencia de adquisición de WMDRM no \_ \_ \_ es silenciosa, salvo que se creará un desafío de licencia de la versión 1 de DRM.</span><span class="sxs-lookup"><span data-stu-id="ef30a-134">The same as WMDRM\_ACQUIRE\_LICENSE\_NONSILENT, except that a DRM version 1 license challenge will be created.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="ef30a-135">*ppunkCancelationCookie* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ef30a-135">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef30a-136">Puntero que recibe un puntero a la interfaz **IUnknown** de un objeto que identifica esta llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="ef30a-136">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="ef30a-137">Este puntero de interfaz se puede usar para cancelar la llamada asincrónica llamando al método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="ef30a-137">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef30a-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef30a-138">Return value</span></span>

<span data-ttu-id="ef30a-139">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ef30a-139">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ef30a-140">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="ef30a-140">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ef30a-141">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ef30a-141">Return code</span></span>                                                                          | <span data-ttu-id="ef30a-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef30a-142">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ef30a-143"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ef30a-143"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ef30a-144">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="ef30a-144">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ef30a-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef30a-145">Remarks</span></span>

<span data-ttu-id="ef30a-146">Este método se ejecuta de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="ef30a-146">This method executes asynchronously.</span></span> <span data-ttu-id="ef30a-147">Vuelve inmediatamente después de llamarlo y, a continuación, genera un evento **MEWMDRMLicenseAcquisitionCompleted** cuando se completa el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="ef30a-147">It returns immediately after being called and then generates an **MEWMDRMLicenseAcquisitionCompleted** event when processing is complete.</span></span> <span data-ttu-id="ef30a-148">Para las operaciones de adquisición de licencias no silenciosas, el valor del evento obtenido mediante una llamada a **IMFMediaEvent:: GetValue** es un puntero **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="ef30a-148">For non-silent license acquisition operations, the value of the event obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="ef30a-149">Puede llamar al método **QueryInterface** de la interfaz **IUnknown** recuperada para obtener una instancia de la interfaz [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) .</span><span class="sxs-lookup"><span data-stu-id="ef30a-149">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) interface.</span></span>

<span data-ttu-id="ef30a-150">Para obtener más información sobre el uso de los métodos asincrónicos de las API extendidas del cliente DRM de Windows Media, vea [usar el modelo de eventos de Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="ef30a-150">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef30a-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef30a-151">Requirements</span></span>



| <span data-ttu-id="ef30a-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef30a-152">Requirement</span></span> | <span data-ttu-id="ef30a-153">Value</span><span class="sxs-lookup"><span data-stu-id="ef30a-153">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef30a-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef30a-154">Header</span></span><br/>  | <dl> <span data-ttu-id="ef30a-155"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef30a-155"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef30a-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ef30a-156">Library</span></span><br/> | <dl> <span data-ttu-id="ef30a-157"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef30a-157"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef30a-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef30a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef30a-159">**Interfaz IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="ef30a-159">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> <dt>

[<span data-ttu-id="ef30a-160">**Adquisición de licencias silenciosa**</span><span class="sxs-lookup"><span data-stu-id="ef30a-160">**Silent License Acquisition**</span></span>](silent-license-acquisition.md)
</dt> </dl>

 

 





