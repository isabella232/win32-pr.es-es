---
title: Método IWMDRMNetTransmitter SetLicenseChallenge (wmdrmsdk. h)
description: El método SetLicenseChallenge procesa un desafío de licencia enviado por un receptor de Windows Media DRM para dispositivos de red.
ms.assetid: 3d4cd029-a8f5-49fc-ba8c-d8615ff94366
keywords:
- Método SetLicenseChallenge formato de Windows Media
- Método SetLicenseChallenge formato de Windows Media, interfaz IWMDRMNetTransmitter
- Interfaz IWMDRMNetTransmitter formato de Windows Media, método SetLicenseChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.SetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94b83ca615896039a592d147fe8c14d15493cec0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679140"
---
# <a name="iwmdrmnettransmittersetlicensechallenge-method"></a><span data-ttu-id="0984e-106">IWMDRMNetTransmitter:: SetLicenseChallenge (método)</span><span class="sxs-lookup"><span data-stu-id="0984e-106">IWMDRMNetTransmitter::SetLicenseChallenge method</span></span>

<span data-ttu-id="0984e-107">El método **SetLicenseChallenge** procesa un desafío de licencia enviado por un receptor de Windows Media DRM para dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="0984e-107">The **SetLicenseChallenge** method processes a license challenge sent by a Windows Media DRM for Network Devices receiver.</span></span>

## <a name="syntax"></a><span data-ttu-id="0984e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0984e-108">Syntax</span></span>


```C++
HRESULT SetLicenseChallenge(
  [in] BYTE  *pbLicenseChallenge,
  [in] DWORD cbLicenseChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="0984e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0984e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0984e-110">*pbLicenseChallenge* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0984e-110">*pbLicenseChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0984e-111">Puntero a los datos de desafío de licencia enviados por un receptor.</span><span class="sxs-lookup"><span data-stu-id="0984e-111">Pointer to the license challenge data that was sent by a receiver.</span></span>

</dd> <dt>

<span data-ttu-id="0984e-112">*cbLicenseChallenge* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0984e-112">*cbLicenseChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0984e-113">Tamaño del desafío de la licencia en bytes.</span><span class="sxs-lookup"><span data-stu-id="0984e-113">Size of license challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0984e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0984e-114">Return value</span></span>

<span data-ttu-id="0984e-115">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0984e-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0984e-116">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="0984e-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0984e-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0984e-117">Return code</span></span>                                                                          | <span data-ttu-id="0984e-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="0984e-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0984e-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0984e-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0984e-120">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="0984e-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0984e-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0984e-121">Remarks</span></span>

<span data-ttu-id="0984e-122">Si este método se ejecuta correctamente, las llamadas subsiguientes a los otros métodos de **IWMDRMNetTransmitter** utilizarán la información del desafío procesado.</span><span class="sxs-lookup"><span data-stu-id="0984e-122">If this method succeeds, subsequent calls to the other methods of **IWMDRMNetTransmitter** will use the information in the processed challenge.</span></span>

## <a name="requirements"></a><span data-ttu-id="0984e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0984e-123">Requirements</span></span>



| <span data-ttu-id="0984e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0984e-124">Requirement</span></span> | <span data-ttu-id="0984e-125">Value</span><span class="sxs-lookup"><span data-stu-id="0984e-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0984e-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0984e-126">Header</span></span><br/> | <dl> <span data-ttu-id="0984e-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="0984e-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0984e-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0984e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0984e-129">**Interfaz IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="0984e-129">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





