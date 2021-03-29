---
title: Método IWMDRMNetReceiver GetRegistrationChallenge (wmdrmsdk. h)
description: El método GetRegistrationChallenge genera un mensaje de desafío de registro de DRM de Windows Media para dispositivos de red.
ms.assetid: 7b3641a1-ccc5-4e29-b0e9-808b111f8841
keywords:
- Método GetRegistrationChallenge formato de Windows Media
- Método GetRegistrationChallenge formato de Windows Media, interfaz IWMDRMNetReceiver
- Interfaz IWMDRMNetReceiver formato de Windows Media, método GetRegistrationChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetRegistrationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a292749e95ca6ba2dabc8f3829eae827dbdd8325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680908"
---
# <a name="iwmdrmnetreceivergetregistrationchallenge-method"></a><span data-ttu-id="22383-106">IWMDRMNetReceiver:: GetRegistrationChallenge (método)</span><span class="sxs-lookup"><span data-stu-id="22383-106">IWMDRMNetReceiver::GetRegistrationChallenge method</span></span>

<span data-ttu-id="22383-107">El método **GetRegistrationChallenge** genera un mensaje de desafío de registro de DRM de Windows Media para dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="22383-107">The **GetRegistrationChallenge** method generates a Windows Media DRM for Network Devices registration challenge message.</span></span>

## <a name="syntax"></a><span data-ttu-id="22383-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22383-108">Syntax</span></span>


```C++
HRESULT GetRegistrationChallenge(
  [out] BYTE  **ppbRegistrationChallenge,
  [out] DWORD *pcbRegistrationChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="22383-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22383-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22383-110">*ppbRegistrationChallenge* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="22383-110">*ppbRegistrationChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22383-111">Dirección de un puntero que recibe la dirección del desafío generado.</span><span class="sxs-lookup"><span data-stu-id="22383-111">Address of a pointer that receives the address of the generated challenge.</span></span> <span data-ttu-id="22383-112">Cuando termine con estos datos, debe liberar la memoria mediante una llamada a **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="22383-112">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="22383-113">*pcbRegistrationChallenge* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="22383-113">*pcbRegistrationChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22383-114">Dirección de una variable que recibe el tamaño del desafío de registro en bytes.</span><span class="sxs-lookup"><span data-stu-id="22383-114">Address of a variable that receives the size of the registration challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22383-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22383-115">Return value</span></span>

<span data-ttu-id="22383-116">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="22383-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="22383-117">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="22383-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="22383-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="22383-118">Return code</span></span>                                                                          | <span data-ttu-id="22383-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="22383-119">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="22383-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="22383-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="22383-121">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="22383-121">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="22383-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22383-122">Remarks</span></span>

<span data-ttu-id="22383-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="22383-123">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="22383-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22383-124">Requirements</span></span>



| <span data-ttu-id="22383-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="22383-125">Requirement</span></span> | <span data-ttu-id="22383-126">Value</span><span class="sxs-lookup"><span data-stu-id="22383-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22383-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22383-127">Header</span></span><br/> | <dl> <span data-ttu-id="22383-128"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="22383-128"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22383-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="22383-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22383-130">**Interfaz IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="22383-130">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="22383-131">**IWMDRMNetReceiver::P rocessRegistrationResponse**</span><span class="sxs-lookup"><span data-stu-id="22383-131">**IWMDRMNetReceiver::ProcessRegistrationResponse**</span></span>](iwmdrmnetreceiver-processregistrationresponse.md)
</dt> </dl>

 

 





