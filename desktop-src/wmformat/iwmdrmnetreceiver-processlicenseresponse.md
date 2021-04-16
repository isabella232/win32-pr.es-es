---
title: Método IWMDRMNetReceiver ProcessLicenseResponse (wmdrmsdk. h)
description: El método ProcessLicenseResponse procesa la respuesta de la licencia enviada por el transmisor en respuesta a un desafío de licencia.
ms.assetid: b6d04651-746b-474e-8a02-6b7cbee9db46
keywords:
- Método ProcessLicenseResponse formato de Windows Media
- Método ProcessLicenseResponse formato de Windows Media, interfaz IWMDRMNetReceiver
- Interfaz IWMDRMNetReceiver formato de Windows Media, método ProcessLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a09ebab81b71e21b9ef922423a7bbe67b20596
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679143"
---
# <a name="iwmdrmnetreceiverprocesslicenseresponse-method"></a><span data-ttu-id="5bcd5-106">IWMDRMNetReceiver::P método rocessLicenseResponse</span><span class="sxs-lookup"><span data-stu-id="5bcd5-106">IWMDRMNetReceiver::ProcessLicenseResponse method</span></span>

<span data-ttu-id="5bcd5-107">El método **ProcessLicenseResponse** procesa la respuesta de la licencia enviada por el transmisor en respuesta a un desafío de licencia.</span><span class="sxs-lookup"><span data-stu-id="5bcd5-107">The **ProcessLicenseResponse** method processes the license response that is sent by the transmitter in reply to a license challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bcd5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5bcd5-108">Syntax</span></span>


```C++
HRESULT ProcessLicenseResponse(
  [in]  BYTE  *pbLicenseResponse,
  [in]  DWORD cbLicenseResponse,
  [out] BYTE  **ppbWMDRMNetLicenseRepresentation,
  [out] DWORD *pcbWMDRMNetLicenseRepresentation
);
```



## <a name="parameters"></a><span data-ttu-id="5bcd5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5bcd5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bcd5-110">*pbLicenseResponse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5bcd5-110">*pbLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bcd5-111">Respuesta de licencia recibida del transmisor.</span><span class="sxs-lookup"><span data-stu-id="5bcd5-111">License response received from the transmitter.</span></span>

</dd> <dt>

<span data-ttu-id="5bcd5-112">*cbLicenseResponse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5bcd5-112">*cbLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bcd5-113">Tamaño de la respuesta en bytes.</span><span class="sxs-lookup"><span data-stu-id="5bcd5-113">Size of the response in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5bcd5-114">*ppbWMDRMNetLicenseRepresentation* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5bcd5-114">*ppbWMDRMNetLicenseRepresentation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bcd5-115">Dirección de una variable que recibe la dirección de la representación de la licencia interna para la licencia incluida en el mensaje de respuesta de la licencia.</span><span class="sxs-lookup"><span data-stu-id="5bcd5-115">Address of a variable that receives the address of the internal license representation for the license contained in the license response message.</span></span> <span data-ttu-id="5bcd5-116">Cuando termine con estos datos, debe liberar la memoria mediante una llamada a **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="5bcd5-116">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span> <span data-ttu-id="5bcd5-117">Este parámetro se puede establecer en **null** si no se necesita la representación de la licencia.</span><span class="sxs-lookup"><span data-stu-id="5bcd5-117">This parameter may be set to **NULL** if the license representation is not needed.</span></span>

</dd> <dt>

<span data-ttu-id="5bcd5-118">*pcbWMDRMNetLicenseRepresentation* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5bcd5-118">*pcbWMDRMNetLicenseRepresentation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bcd5-119">Dirección de una variable que recibe el tamaño de la representación de la licencia.</span><span class="sxs-lookup"><span data-stu-id="5bcd5-119">Address of a variable that receives the size of the license representation.</span></span> <span data-ttu-id="5bcd5-120">Debe establecerse en **null** si *ppbWMDRMNetLicenseRepresentation* es **null**.</span><span class="sxs-lookup"><span data-stu-id="5bcd5-120">Must be set to **NULL** if *ppbWMDRMNetLicenseRepresentation* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bcd5-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5bcd5-121">Return value</span></span>

<span data-ttu-id="5bcd5-122">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5bcd5-122">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5bcd5-123">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="5bcd5-123">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5bcd5-124">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5bcd5-124">Return code</span></span>                                                                                                | <span data-ttu-id="5bcd5-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="5bcd5-125">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="5bcd5-126"><dt>**NS \_ E \_ DRM \_ RIV \_ demasiado \_ pequeño**</dt></span><span class="sxs-lookup"><span data-stu-id="5bcd5-126"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="5bcd5-127">Se necesita una lista de revocación de contenido actualizada.</span><span class="sxs-lookup"><span data-stu-id="5bcd5-127">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="5bcd5-128"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="5bcd5-128"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="5bcd5-129">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="5bcd5-129">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="5bcd5-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5bcd5-130">Remarks</span></span>

<span data-ttu-id="5bcd5-131">La respuesta de licencia procesada mediante este método debe corresponder al último desafío de licencia generado en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="5bcd5-131">The license response processed by using this method must correspond to the last license challenge generated on the client computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bcd5-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bcd5-132">Requirements</span></span>



| <span data-ttu-id="5bcd5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bcd5-133">Requirement</span></span> | <span data-ttu-id="5bcd5-134">Value</span><span class="sxs-lookup"><span data-stu-id="5bcd5-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5bcd5-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5bcd5-135">Header</span></span><br/> | <dl> <span data-ttu-id="5bcd5-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bcd5-136"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bcd5-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bcd5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bcd5-138">**Interfaz IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="5bcd5-138">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="5bcd5-139">**IWMDRMNetReceiver::GetLicenseChallenge**</span><span class="sxs-lookup"><span data-stu-id="5bcd5-139">**IWMDRMNetReceiver::GetLicenseChallenge**</span></span>](iwmdrmnetreceiver-getlicensechallenge.md)
</dt> </dl>

 

 





