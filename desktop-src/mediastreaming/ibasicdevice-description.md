---
title: IBasicDevice Description (método)
description: Recupera una descripción del dispositivo.
ms.assetid: 9973AC46-E6BA-4931-BDEB-E64B147AB291
keywords:
- Description (método) API de streaming de multimedia
- Description (método) API de streaming de media, interfaz IBasicDevice
- IBasicDevice interface media streaming API, Description (método)
topic_type:
- apiref
api_name:
- IBasicDevice.Description
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f094246d1424c458e624d4a49358b63a84b9b7d2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076622"
---
# <a name="ibasicdevicedescription-method"></a><span data-ttu-id="8760f-106">IBasicDevice::D método Descripción</span><span class="sxs-lookup"><span data-stu-id="8760f-106">IBasicDevice::Description method</span></span>

<span data-ttu-id="8760f-107">Recupera una descripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8760f-107">Retrieves a description of the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="8760f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8760f-108">Syntax</span></span>


```C++
HRESULT Description(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="8760f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8760f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8760f-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8760f-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8760f-111">Recibe un puntero a la descripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8760f-111">Receives a pointer to the description of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8760f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8760f-112">Return value</span></span>

<span data-ttu-id="8760f-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8760f-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8760f-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="8760f-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8760f-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8760f-115">Return code</span></span>                                                                          | <span data-ttu-id="8760f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="8760f-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8760f-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8760f-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8760f-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="8760f-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="8760f-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="8760f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8760f-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="8760f-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





