---
title: Método IWMDRMNetReceiver ProcessRegistrationResponse (wmdrmsdk. h)
description: El método ProcessRegistrationResponse procesa una respuesta de registro enviada por el transmisor en respuesta a un desafío de registro.
ms.assetid: d0260e93-0a5e-494b-a723-bb62206ed55b
keywords:
- Método ProcessRegistrationResponse formato de Windows Media
- Método ProcessRegistrationResponse formato de Windows Media, interfaz IWMDRMNetReceiver
- Interfaz IWMDRMNetReceiver formato de Windows Media, método ProcessRegistrationResponse
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessRegistrationResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77b01f443d57825d82b7cf9556d7585745bb99e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679142"
---
# <a name="iwmdrmnetreceiverprocessregistrationresponse-method"></a><span data-ttu-id="0fc62-106">IWMDRMNetReceiver::P método rocessRegistrationResponse</span><span class="sxs-lookup"><span data-stu-id="0fc62-106">IWMDRMNetReceiver::ProcessRegistrationResponse method</span></span>

<span data-ttu-id="0fc62-107">El método **ProcessRegistrationResponse** procesa una respuesta de registro enviada por el transmisor en respuesta a un desafío de registro.</span><span class="sxs-lookup"><span data-stu-id="0fc62-107">The **ProcessRegistrationResponse** method processes a registration response sent by the transmitter in reply to a registration challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fc62-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0fc62-108">Syntax</span></span>


```C++
HRESULT ProcessRegistrationResponse(
  [in]  BYTE     *pbRegistrationResponse,
  [in]  DWORD    cbRegistrationResponse,
  [out] IUnknown **ppunkCancellationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="0fc62-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0fc62-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fc62-110">*pbRegistrationResponse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0fc62-110">*pbRegistrationResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fc62-111">Respuesta de registro recibida del transmisor.</span><span class="sxs-lookup"><span data-stu-id="0fc62-111">Registration response received from the transmitter.</span></span>

</dd> <dt>

<span data-ttu-id="0fc62-112">*cbRegistrationResponse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0fc62-112">*cbRegistrationResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fc62-113">Tamaño de la respuesta de registro en bytes.</span><span class="sxs-lookup"><span data-stu-id="0fc62-113">Size of the registration response in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0fc62-114">*ppunkCancellationCookie* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0fc62-114">*ppunkCancellationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fc62-115">Puntero que recibe un puntero a la interfaz **IUnknown** de un objeto que identifica esta llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="0fc62-115">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="0fc62-116">Este puntero de interfaz se puede usar para cancelar la llamada asincrónica llamando al método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="0fc62-116">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fc62-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0fc62-117">Return value</span></span>

<span data-ttu-id="0fc62-118">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0fc62-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0fc62-119">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="0fc62-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0fc62-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0fc62-120">Return code</span></span>                                                                          | <span data-ttu-id="0fc62-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fc62-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0fc62-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0fc62-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0fc62-123">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="0fc62-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0fc62-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0fc62-124">Remarks</span></span>

<span data-ttu-id="0fc62-125">Este método se ejecuta de forma asincrónica; una vez completado el procesamiento, el evento MEProximityCompleted se envía a la interfaz **IMFMediaEventGenerator** .</span><span class="sxs-lookup"><span data-stu-id="0fc62-125">This method executes asynchronously; when processing is complete, the MEProximityCompleted event is sent to the **IMFMediaEventGenerator** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fc62-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fc62-126">Requirements</span></span>



| <span data-ttu-id="0fc62-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fc62-127">Requirement</span></span> | <span data-ttu-id="0fc62-128">Value</span><span class="sxs-lookup"><span data-stu-id="0fc62-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0fc62-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0fc62-129">Header</span></span><br/> | <dl> <span data-ttu-id="0fc62-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fc62-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fc62-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="0fc62-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fc62-132">**Interfaz IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="0fc62-132">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="0fc62-133">**IWMDRMNetReceiver::GetRegistrationChallenge**</span><span class="sxs-lookup"><span data-stu-id="0fc62-133">**IWMDRMNetReceiver::GetRegistrationChallenge**</span></span>](iwmdrmnetreceiver-getregistrationchallenge.md)
</dt> </dl>

 

 





