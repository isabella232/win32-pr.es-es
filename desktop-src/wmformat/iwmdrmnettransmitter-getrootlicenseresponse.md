---
title: Método IWMDRMNetTransmitter GetRootLicenseResponse (wmdrmsdk. h)
description: El método GetRootLicenseResponse genera un mensaje de respuesta de licencia raíz.
ms.assetid: c735ee52-f0e0-4404-881b-18ee9a7fa9f9
keywords:
- Método GetRootLicenseResponse formato de Windows Media
- Método GetRootLicenseResponse formato de Windows Media, interfaz IWMDRMNetTransmitter
- Interfaz IWMDRMNetTransmitter formato de Windows Media, método GetRootLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetRootLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3497a3eaedb872b7d2c9eb5d7782d01f8b35462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679484"
---
# <a name="iwmdrmnettransmittergetrootlicenseresponse-method"></a><span data-ttu-id="2e201-106">IWMDRMNetTransmitter:: GetRootLicenseResponse (método)</span><span class="sxs-lookup"><span data-stu-id="2e201-106">IWMDRMNetTransmitter::GetRootLicenseResponse method</span></span>

<span data-ttu-id="2e201-107">El método **GetRootLicenseResponse** genera un mensaje de respuesta de licencia raíz.</span><span class="sxs-lookup"><span data-stu-id="2e201-107">The **GetRootLicenseResponse** method generates a root license response message.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e201-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e201-108">Syntax</span></span>


```C++
HRESULT GetRootLicenseResponse(
  [in]  BSTR  bstrKID,
  [out] BYTE  **ppbLicenseResponse,
  [out] DWORD *pcbLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="2e201-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e201-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e201-110">*bstrKID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2e201-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e201-111">Identificador de clave codificado en Base64 que se va a usar para la nueva licencia raíz.</span><span class="sxs-lookup"><span data-stu-id="2e201-111">Base64-encoded key identifier to be used for the new root license.</span></span> <span data-ttu-id="2e201-112">El identificador de clave debe ser un valor GUID generado aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="2e201-112">The key identifier should be a randomly generated GUID value.</span></span>

</dd> <dt>

<span data-ttu-id="2e201-113">*ppbLicenseResponse* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2e201-113">*ppbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e201-114">Dirección de una variable que recibe la dirección de la respuesta de licencia generada.</span><span class="sxs-lookup"><span data-stu-id="2e201-114">Address of a variable that receives the address of the generated license response.</span></span> <span data-ttu-id="2e201-115">Cuando termine con estos datos, debe liberar la memoria mediante una llamada a **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="2e201-115">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="2e201-116">*pcbLicenseResponse* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2e201-116">*pcbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e201-117">Dirección de una variable que recibe el tamaño de la respuesta de la licencia, en bytes.</span><span class="sxs-lookup"><span data-stu-id="2e201-117">Address of a variable that receives the size of the license response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e201-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e201-118">Return value</span></span>

<span data-ttu-id="2e201-119">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2e201-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2e201-120">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="2e201-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2e201-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2e201-121">Return code</span></span>                                                                                                | <span data-ttu-id="2e201-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e201-122">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="2e201-123"><dt>**NS \_ E \_ DRM \_ RIV \_ demasiado \_ pequeño**</dt></span><span class="sxs-lookup"><span data-stu-id="2e201-123"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="2e201-124">Se necesita una lista de revocación de contenido actualizada.</span><span class="sxs-lookup"><span data-stu-id="2e201-124">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="2e201-125"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2e201-125"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="2e201-126">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="2e201-126">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="2e201-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e201-127">Remarks</span></span>

<span data-ttu-id="2e201-128">La licencia raíz generada se crea con la información de los datos del desafío de la licencia, que se procesa para la interfaz llamando a [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md).</span><span class="sxs-lookup"><span data-stu-id="2e201-128">The generated root license is created using the information from the license challenge data, which is processed for the interface by calling [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md).</span></span>

<span data-ttu-id="2e201-129">La licencia raíz se usa en la generación de licencias de hoja, lo que se logra mediante una llamada al método [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="2e201-129">The root license is used in the generation of leaf licenses, which is accomplished by calling the [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) method.</span></span> <span data-ttu-id="2e201-130">La interfaz **IWMDRMNetTransmitter** mantiene una copia de la licencia raíz para ese uso.</span><span class="sxs-lookup"><span data-stu-id="2e201-130">The **IWMDRMNetTransmitter** interface maintains a copy of the root license for that use.</span></span>

<span data-ttu-id="2e201-131">La licencia raíz creada mediante una llamada a este método no tiene directivas y está configurada para que no se pueda conservar en el dispositivo receptor.</span><span class="sxs-lookup"><span data-stu-id="2e201-131">The root license created by calling this method does not have any policies and is configured so that it cannot be persisted on the receiving device.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e201-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e201-132">Requirements</span></span>



| <span data-ttu-id="2e201-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e201-133">Requirement</span></span> | <span data-ttu-id="2e201-134">Value</span><span class="sxs-lookup"><span data-stu-id="2e201-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e201-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e201-135">Header</span></span><br/> | <dl> <span data-ttu-id="2e201-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e201-136"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e201-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e201-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e201-138">**Interfaz IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="2e201-138">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





