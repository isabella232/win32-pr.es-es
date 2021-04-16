---
title: Método IWMDRMSecurity GetContentEnablersForRevocations (wmdrmsdk. h)
description: El método GetContentEnablersForRevocations recupera interfaces del habilitador de contenido que permiten la renovación de componentes basados en certificados revocados.
ms.assetid: 9e5b58b8-07d6-4607-a40f-cd7df4984ac5
keywords:
- Método GetContentEnablersForRevocations formato de Windows Media
- Método GetContentEnablersForRevocations formato de Windows Media, interfaz IWMDRMSecurity
- Interfaz IWMDRMSecurity formato de Windows Media, método GetContentEnablersForRevocations
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersForRevocations
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd47ac3b44a1d74cb42113513a44c4b48689a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649760"
---
# <a name="iwmdrmsecuritygetcontentenablersforrevocations-method"></a><span data-ttu-id="86d98-106">IWMDRMSecurity:: GetContentEnablersForRevocations (método)</span><span class="sxs-lookup"><span data-stu-id="86d98-106">IWMDRMSecurity::GetContentEnablersForRevocations method</span></span>

<span data-ttu-id="86d98-107">El método **GetContentEnablersForRevocations** recupera interfaces del habilitador de contenido que permiten la renovación de componentes basados en certificados revocados.</span><span class="sxs-lookup"><span data-stu-id="86d98-107">The **GetContentEnablersForRevocations** method retrieves content enabler interfaces that enable renewal of components based on revoked certificates.</span></span>

## <a name="syntax"></a><span data-ttu-id="86d98-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86d98-108">Syntax</span></span>


```C++
HRESULT GetContentEnablersForRevocations(
  [in]      BYTE              **rgpbCerts,
  [in]      DWORD             *rgpdwCertSizes,
  [in]      GUID              **rgpguidCerts,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a><span data-ttu-id="86d98-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86d98-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86d98-110">*rgpbCerts* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86d98-110">*rgpbCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86d98-111">Matriz de certificados para los que se van a recuperar los habilitadores de contenido.</span><span class="sxs-lookup"><span data-stu-id="86d98-111">Array of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="86d98-112">El número de elementos de la matriz debe especificarse mediante *cCerts*.</span><span class="sxs-lookup"><span data-stu-id="86d98-112">The number of elements in the array must be specified by *cCerts*.</span></span>

</dd> <dt>

<span data-ttu-id="86d98-113">*rgpdwCertSizes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86d98-113">*rgpdwCertSizes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86d98-114">Matriz que contiene los tamaños de los certificados en la matriz *rgpbCerts* .</span><span class="sxs-lookup"><span data-stu-id="86d98-114">Array containing the sizes of the certificates in the *rgpbCerts* array.</span></span> <span data-ttu-id="86d98-115">El número de elementos de la matriz debe especificarse mediante *cCerts*.</span><span class="sxs-lookup"><span data-stu-id="86d98-115">The number of elements in the array must be specified by *cCerts*.</span></span>

</dd> <dt>

<span data-ttu-id="86d98-116">*rgpguidCerts* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86d98-116">*rgpguidCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86d98-117">Matriz que contiene los tipos de los certificados de la matriz *rgpbCerts* .</span><span class="sxs-lookup"><span data-stu-id="86d98-117">Array containing the types of the certificates in the *rgpbCerts* array.</span></span> <span data-ttu-id="86d98-118">El número de elementos de la matriz debe especificarse mediante *cCerts*.</span><span class="sxs-lookup"><span data-stu-id="86d98-118">The number of elements in the array must be specified by *cCerts*.</span></span> <span data-ttu-id="86d98-119">Para cada elemento de la matriz, use uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="86d98-119">For each element of the array, use one of the following values.</span></span>



| <span data-ttu-id="86d98-120">Constante GUID</span><span class="sxs-lookup"><span data-stu-id="86d98-120">GUID constant</span></span>                 | <span data-ttu-id="86d98-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="86d98-121">Description</span></span>                                                    |
|-------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="86d98-122">\_aplicación REVOCATIONTYPE de WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="86d98-122">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="86d98-123">Especifica un certificado de aplicación.</span><span class="sxs-lookup"><span data-stu-id="86d98-123">Specifies an application certificate.</span></span>                          |
| <span data-ttu-id="86d98-124">\_dispositivo REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="86d98-124">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="86d98-125">Especifica un certificado de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="86d98-125">Specifies a device certificate.</span></span>                                |
| <span data-ttu-id="86d98-126">\_CARDEA REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="86d98-126">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="86d98-127">Especifica un certificado DRM de Windows Media para dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="86d98-127">Specifies a Windows Media DRM for Network Devices certificate.</span></span> |



 

</dd> <dt>

<span data-ttu-id="86d98-128">*cCerts* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86d98-128">*cCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86d98-129">Número de certificados para los que se van a recuperar los habilitadores de contenido.</span><span class="sxs-lookup"><span data-stu-id="86d98-129">Number of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="86d98-130">Este es el número de elementos de la matriz *rgpbCerts* , la matriz *rgpdwCertSizes* y la matriz *rgpguidCerts* .</span><span class="sxs-lookup"><span data-stu-id="86d98-130">This is the number of elements in the *rgpbCerts* array, the *rgpdwCertSizes* array, and the *rgpguidCerts* array.</span></span>

</dd> <dt>

<span data-ttu-id="86d98-131">*hResultHint* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86d98-131">*hResultHint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86d98-132">Valor devuelto recibido de la operación que produjo un error debido a un certificado revocado.</span><span class="sxs-lookup"><span data-stu-id="86d98-132">Return value received from the operation that failed due to a revoked certificate.</span></span> <span data-ttu-id="86d98-133">Si no llama a en respuesta a una llamada al método con errores, establezca en es \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="86d98-133">If you are not calling in response to a failed method call, set to S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="86d98-134">*prgContentEnablers* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="86d98-134">*prgContentEnablers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86d98-135">Matriz que recibe las direcciones de las interfaces **IMFContentEnabler** recién creadas.</span><span class="sxs-lookup"><span data-stu-id="86d98-135">Array that receives the addresses of the newly created **IMFContentEnabler** interfaces.</span></span> <span data-ttu-id="86d98-136">Establezca en **null** para obtener el número de habilitadores de contenido en el parámetro *pcContentEnablers* .</span><span class="sxs-lookup"><span data-stu-id="86d98-136">Set to **NULL** to get the number of content enablers in the *pcContentEnablers* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="86d98-137">*pcContentEnablers* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="86d98-137">*pcContentEnablers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="86d98-138">Número de elementos de la matriz *prgContentEnablers* .</span><span class="sxs-lookup"><span data-stu-id="86d98-138">Number of elements in the *prgContentEnablers* array.</span></span> <span data-ttu-id="86d98-139">Si *prgContentEnablers* es **null**, este valor se establece en el número de habilitadores de contenido necesarios en la salida.</span><span class="sxs-lookup"><span data-stu-id="86d98-139">If *prgContentEnablers* is **NULL**, this value is set to the number of needed content enablers on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86d98-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86d98-140">Return value</span></span>

<span data-ttu-id="86d98-141">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="86d98-141">The method returns an **HRESULT**.</span></span> <span data-ttu-id="86d98-142">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="86d98-142">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="86d98-143">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="86d98-143">Return code</span></span>                                                                          | <span data-ttu-id="86d98-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="86d98-144">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="86d98-145"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="86d98-145"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="86d98-146">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="86d98-146">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="86d98-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86d98-147">Remarks</span></span>

<span data-ttu-id="86d98-148">Si usa la interfaz **IMFContentEnabler** para renovar los componentes revocados, debe aclarar el proceso al usuario.</span><span class="sxs-lookup"><span data-stu-id="86d98-148">If you use the **IMFContentEnabler** interface to renew revoked components, you must clarify the process to the user.</span></span> <span data-ttu-id="86d98-149">Esta Aclaración debe realizarse porque el proceso de actualización envía información desde el equipo cliente a un sitio web de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="86d98-149">This clarification must be made because the update process sends information from the client computer to a Microsoft Web site.</span></span>

<span data-ttu-id="86d98-150">Cuando se llama a **IMFContentEnabler:: AutomaticEnable**, el habilitador de contenido inicia el explorador predeterminado con la dirección del servicio de actualización en el sitio web de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="86d98-150">When you call **IMFContentEnabler::AutomaticEnable**, the content enabler launches the default browser with the address of the update service on the Microsoft Web site.</span></span> <span data-ttu-id="86d98-151">Un identificador único que identifica el componente revocado se envía al servicio de actualización.</span><span class="sxs-lookup"><span data-stu-id="86d98-151">A unique identifier that identifies the revoked component is sent to the update service.</span></span> <span data-ttu-id="86d98-152">A continuación, el servicio redirige el explorador a una página web desde la que el usuario puede descargar e instalar la nueva versión del componente revocado.</span><span class="sxs-lookup"><span data-stu-id="86d98-152">The service then redirects the browser to a Web page from which the user may be able to download and install the new version of the revoked component.</span></span>

## <a name="requirements"></a><span data-ttu-id="86d98-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86d98-153">Requirements</span></span>



| <span data-ttu-id="86d98-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="86d98-154">Requirement</span></span> | <span data-ttu-id="86d98-155">Value</span><span class="sxs-lookup"><span data-stu-id="86d98-155">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86d98-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86d98-156">Header</span></span><br/>  | <dl> <span data-ttu-id="86d98-157"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="86d98-157"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="86d98-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86d98-158">Library</span></span><br/> | <dl> <span data-ttu-id="86d98-159"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86d98-159"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86d98-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="86d98-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86d98-161">**Revocación y renovación de componentes automatizados**</span><span class="sxs-lookup"><span data-stu-id="86d98-161">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="86d98-162">**Interfaz IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="86d98-162">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





