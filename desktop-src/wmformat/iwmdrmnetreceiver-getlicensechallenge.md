---
title: Método IWMDRMNetReceiver GetLicenseChallenge (wmdrmsdk. h)
description: El método GetLicenseChallenge genera un desafío de licencia de DRM de Windows Media para dispositivos de red que se puede enviar a un transmisor al solicitar contenido protegido.
ms.assetid: c13b9e9e-b076-411b-a106-b602544faaba
keywords:
- Método GetLicenseChallenge formato de Windows Media
- Método GetLicenseChallenge formato de Windows Media, interfaz IWMDRMNetReceiver
- Interfaz IWMDRMNetReceiver formato de Windows Media, método GetLicenseChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f58b85b8dc5edd6c23e809dda8c18bf30137f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679144"
---
# <a name="iwmdrmnetreceivergetlicensechallenge-method"></a><span data-ttu-id="362b3-106">IWMDRMNetReceiver:: GetLicenseChallenge (método)</span><span class="sxs-lookup"><span data-stu-id="362b3-106">IWMDRMNetReceiver::GetLicenseChallenge method</span></span>

<span data-ttu-id="362b3-107">El método **GetLicenseChallenge** genera un desafío de licencia de DRM de Windows Media para dispositivos de red que se puede enviar a un transmisor al solicitar contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="362b3-107">The **GetLicenseChallenge** method generates a Windows Media DRM for Network Devices license challenge that can be sent to a transmitter when requesting protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="362b3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="362b3-108">Syntax</span></span>


```C++
HRESULT GetLicenseChallenge(
  [in]  BSTR  bstrAction,
  [out] BYTE  **ppbLicenseChallenge,
  [out] DWORD *pcbLicenseChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="362b3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="362b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="362b3-110">*bstrAction* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="362b3-110">*bstrAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="362b3-111">Acción para la que se va a generar el desafío.</span><span class="sxs-lookup"><span data-stu-id="362b3-111">Action for which to generate the challenge.</span></span>

</dd> <dt>

<span data-ttu-id="362b3-112">*ppbLicenseChallenge* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="362b3-112">*ppbLicenseChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="362b3-113">Dirección de un puntero que se establece en la dirección del desafío generado.</span><span class="sxs-lookup"><span data-stu-id="362b3-113">Address of a pointer that is set to the address of the generated challenge.</span></span> <span data-ttu-id="362b3-114">Cuando termine con estos datos, debe liberar la memoria mediante una llamada a **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="362b3-114">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="362b3-115">*pcbLicenseChallenge* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="362b3-115">*pcbLicenseChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="362b3-116">Dirección de una variable que recibe el tamaño del desafío de la licencia en bytes.</span><span class="sxs-lookup"><span data-stu-id="362b3-116">Address of a variable that receives the size of the license challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="362b3-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="362b3-117">Return value</span></span>

<span data-ttu-id="362b3-118">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="362b3-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="362b3-119">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="362b3-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="362b3-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="362b3-120">Return code</span></span>                                                                          | <span data-ttu-id="362b3-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="362b3-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="362b3-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="362b3-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="362b3-123">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="362b3-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="362b3-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="362b3-124">Remarks</span></span>

<span data-ttu-id="362b3-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="362b3-125">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="362b3-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="362b3-126">Requirements</span></span>



| <span data-ttu-id="362b3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="362b3-127">Requirement</span></span> | <span data-ttu-id="362b3-128">Value</span><span class="sxs-lookup"><span data-stu-id="362b3-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="362b3-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="362b3-129">Header</span></span><br/> | <dl> <span data-ttu-id="362b3-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="362b3-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="362b3-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="362b3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="362b3-132">**Interfaz IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="362b3-132">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="362b3-133">**IWMDRMNetReceiver::P rocessLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="362b3-133">**IWMDRMNetReceiver::ProcessLicenseResponse**</span></span>](iwmdrmnetreceiver-processlicenseresponse.md)
</dt> </dl>

 

 





