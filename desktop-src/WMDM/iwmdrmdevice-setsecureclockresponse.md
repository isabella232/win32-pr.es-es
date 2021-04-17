---
title: IWMDRMDevice SetSecureClockResponse, método
description: El método SetSecureClockResponse establece la respuesta de reloj segura.
ms.assetid: 3f0a1487-d8c4-478d-bfb0-8d09931fd4b6
keywords:
- Método SetSecureClockResponse de Windows Media Administrador de dispositivos
- Método SetSecureClockResponse de Windows Media Administrador de dispositivos, interfaz IWMDRMDevice
- Interfaz IWMDRMDevice de Windows Media Administrador de dispositivos, método SetSecureClockResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetSecureClockResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821aceda734aceb7a80774db05465f31213eec47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698667"
---
# <a name="iwmdrmdevicesetsecureclockresponse-method"></a><span data-ttu-id="3be19-106">IWMDRMDevice:: SetSecureClockResponse (método)</span><span class="sxs-lookup"><span data-stu-id="3be19-106">IWMDRMDevice::SetSecureClockResponse method</span></span>

<span data-ttu-id="3be19-107">El método **SetSecureClockResponse** establece la respuesta de reloj segura.</span><span class="sxs-lookup"><span data-stu-id="3be19-107">The **SetSecureClockResponse** method sets the secure clock response.</span></span>

## <a name="syntax"></a><span data-ttu-id="3be19-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3be19-108">Syntax</span></span>


```C++
HRESULT SetSecureClockResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a><span data-ttu-id="3be19-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3be19-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3be19-110">*pbResponse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3be19-110">*pbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3be19-111">Respuesta de reloj segura que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="3be19-111">The secure clock response to be set.</span></span>

</dd> <dt>

<span data-ttu-id="3be19-112">*cbResponse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3be19-112">*cbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3be19-113">Tamaño especificado de la respuesta de reloj segura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="3be19-113">The specified size of the secure clock response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3be19-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3be19-114">Return value</span></span>

<span data-ttu-id="3be19-115">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3be19-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3be19-116">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="3be19-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3be19-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3be19-117">Return code</span></span>                                                                          | <span data-ttu-id="3be19-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="3be19-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3be19-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3be19-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3be19-120">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="3be19-120">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3be19-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3be19-121">Requirements</span></span>



| <span data-ttu-id="3be19-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3be19-122">Requirement</span></span> | <span data-ttu-id="3be19-123">Value</span><span class="sxs-lookup"><span data-stu-id="3be19-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3be19-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3be19-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3be19-125"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3be19-125"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="3be19-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3be19-126">Library</span></span><br/> | <dl> <span data-ttu-id="3be19-127"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3be19-127"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3be19-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3be19-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3be19-129">**GetSecureClock**</span><span class="sxs-lookup"><span data-stu-id="3be19-129">**GetSecureClock**</span></span>](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[<span data-ttu-id="3be19-130">**Interfaz IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="3be19-130">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





