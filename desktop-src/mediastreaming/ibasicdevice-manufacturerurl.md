---
title: IBasicDevice ManufacturerUrl (método)
description: Recupera la dirección URL del fabricante del dispositivo.
ms.assetid: E8372D15-D8B5-49E4-950A-96B4A88B0450
keywords:
- ManufacturerUrl (método) API de streaming de multimedia
- ManufacturerUrl (método) API de streaming de multimedia, interfaz IBasicDevice
- Interfaz IBasicDevice API de streaming de multimedia, método ManufacturerUrl
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e41ca83c98507c65ead8d1faf2922ee84b45649
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076688"
---
# <a name="ibasicdevicemanufacturerurl-method"></a><span data-ttu-id="e9258-106">IBasicDevice:: ManufacturerUrl (método)</span><span class="sxs-lookup"><span data-stu-id="e9258-106">IBasicDevice::ManufacturerUrl method</span></span>

<span data-ttu-id="e9258-107">Recupera la dirección URL del fabricante del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9258-107">Retrieves the device s manufacturer URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9258-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9258-108">Syntax</span></span>


```C++
HRESULT ManufacturerUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="e9258-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9258-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9258-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e9258-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9258-111">Recibe un puntero a la dirección URL del fabricante del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9258-111">Receives a pointer to the device s manufacturer URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9258-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9258-112">Return value</span></span>

<span data-ttu-id="e9258-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e9258-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e9258-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="e9258-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e9258-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e9258-115">Return code</span></span>                                                                          | <span data-ttu-id="e9258-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9258-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e9258-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e9258-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e9258-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="e9258-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="e9258-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9258-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9258-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="e9258-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





