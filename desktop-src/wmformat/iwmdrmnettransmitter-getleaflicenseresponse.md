---
title: Método IWMDRMNetTransmitter GetLeafLicenseResponse (wmdrmsdk. h)
description: El método GetLeafLicenseResponse genera un mensaje de respuesta de licencia de hoja.
ms.assetid: b2893d22-b6f3-44d2-b6db-e2b07fbe098d
keywords:
- Método GetLeafLicenseResponse formato de Windows Media
- Método GetLeafLicenseResponse formato de Windows Media, interfaz IWMDRMNetTransmitter
- Interfaz IWMDRMNetTransmitter formato de Windows Media, método GetLeafLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetLeafLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf2374966abfae4353a72755313c1cbbdfb7287
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679141"
---
# <a name="iwmdrmnettransmittergetleaflicenseresponse-method"></a><span data-ttu-id="e0b56-106">IWMDRMNetTransmitter:: GetLeafLicenseResponse (método)</span><span class="sxs-lookup"><span data-stu-id="e0b56-106">IWMDRMNetTransmitter::GetLeafLicenseResponse method</span></span>

<span data-ttu-id="e0b56-107">El método **GetLeafLicenseResponse** genera un mensaje de respuesta de licencia de hoja.</span><span class="sxs-lookup"><span data-stu-id="e0b56-107">The **GetLeafLicenseResponse** method generates a leaf license response message.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0b56-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0b56-108">Syntax</span></span>


```C++
HRESULT GetLeafLicenseResponse(
  [in]  BSTR            bstrKID,
  [in]  WMDRMNET_POLICY *pPolicy,
  [out] IWMDRMEncrypt   **ppIWMDRMEncrypt,
  [out] BYTE            **ppbLicenseResponse,
  [out] DWORD           *pcbLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="e0b56-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0b56-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0b56-110">*bstrKID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0b56-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0b56-111">Identificador de clave codificado en Base64 que se va a usar para la nueva licencia de hoja.</span><span class="sxs-lookup"><span data-stu-id="e0b56-111">Base64-encoded key identifier to be used for the new leaf license.</span></span> <span data-ttu-id="e0b56-112">El identificador de clave debe ser un valor GUID generado aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="e0b56-112">The key identifier should be a randomly generated GUID value.</span></span>

</dd> <dt>

<span data-ttu-id="e0b56-113">*pPolicy* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0b56-113">*pPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0b56-114">Puntero a la estructura de [**\_ Directiva WMDRMNET**](wmdrmnet-policy.md) que define la Directiva que se va a usar para la licencia de hoja.</span><span class="sxs-lookup"><span data-stu-id="e0b56-114">Pointer to the [**WMDRMNET\_POLICY**](wmdrmnet-policy.md) structure that defines the policy to use for the leaf license.</span></span>

</dd> <dt>

<span data-ttu-id="e0b56-115">*ppIWMDRMEncrypt* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e0b56-115">*ppIWMDRMEncrypt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0b56-116">Dirección de una variable que recibe un puntero a la interfaz [**IWMDRMEncrypt**](iwmdrmencrypt.md) que se puede usar para cifrar los datos de la nueva licencia de hoja.</span><span class="sxs-lookup"><span data-stu-id="e0b56-116">Address of a variable that receives a pointer to the [**IWMDRMEncrypt**](iwmdrmencrypt.md) interface that can be used to encrypt data for the new leaf license.</span></span>

</dd> <dt>

<span data-ttu-id="e0b56-117">*ppbLicenseResponse* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e0b56-117">*ppbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0b56-118">Dirección de una variable que recibe la dirección de la respuesta de licencia generada.</span><span class="sxs-lookup"><span data-stu-id="e0b56-118">Address of a variable that receives the address of the generated license response.</span></span> <span data-ttu-id="e0b56-119">Cuando termine con estos datos, debe liberar la memoria mediante una llamada a **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="e0b56-119">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="e0b56-120">*pcbLicenseResponse* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e0b56-120">*pcbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0b56-121">Dirección de una variable que recibe el tamaño de la respuesta de la licencia, en bytes.</span><span class="sxs-lookup"><span data-stu-id="e0b56-121">Address of a variable that receives the size of the license response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0b56-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0b56-122">Return value</span></span>

<span data-ttu-id="e0b56-123">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e0b56-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e0b56-124">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="e0b56-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e0b56-125">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e0b56-125">Return code</span></span>                                                                                                | <span data-ttu-id="e0b56-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0b56-126">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="e0b56-127"><dt>**NS \_ E \_ DRM \_ RIV \_ demasiado \_ pequeño**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b56-127"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="e0b56-128">Se necesita una lista de revocación de contenido actualizada.</span><span class="sxs-lookup"><span data-stu-id="e0b56-128">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="e0b56-129"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b56-129"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="e0b56-130">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="e0b56-130">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="e0b56-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0b56-131">Remarks</span></span>

<span data-ttu-id="e0b56-132">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e0b56-132">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0b56-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0b56-133">Requirements</span></span>



| <span data-ttu-id="e0b56-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0b56-134">Requirement</span></span> | <span data-ttu-id="e0b56-135">Value</span><span class="sxs-lookup"><span data-stu-id="e0b56-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0b56-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0b56-136">Header</span></span><br/> | <dl> <span data-ttu-id="e0b56-137"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0b56-137"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0b56-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0b56-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0b56-139">**Interfaz IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="e0b56-139">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





