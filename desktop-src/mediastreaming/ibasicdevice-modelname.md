---
title: IBasicDevice ModelName (método)
description: Recupera el nombre del modelo del dispositivo.
ms.assetid: 8F871E89-97C1-4788-83AB-B7E0D8D6E0B5
keywords:
- Método ModelName API de streaming de multimedia
- Método ModelName API de streaming de multimedia, interfaz IBasicDevice
- Interfaz IBasicDevice streaming de multimedia API, ModelName (método)
topic_type:
- apiref
api_name:
- IBasicDevice.ModelName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e486b372b2108bc85153f416032ef6bfbe8a397
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105676299"
---
# <a name="ibasicdevicemodelname-method"></a><span data-ttu-id="6b5e4-106">IBasicDevice:: ModelName (método)</span><span class="sxs-lookup"><span data-stu-id="6b5e4-106">IBasicDevice::ModelName method</span></span>

<span data-ttu-id="6b5e4-107">Recupera el nombre del modelo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b5e4-107">Retrieves the device s model name.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b5e4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b5e4-108">Syntax</span></span>


```C++
HRESULT ModelName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="6b5e4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b5e4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b5e4-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6b5e4-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b5e4-111">Recibe un puntero al nombre del modelo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b5e4-111">Receives a pointer to the device s model name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b5e4-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b5e4-112">Return value</span></span>

<span data-ttu-id="6b5e4-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6b5e4-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6b5e4-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="6b5e4-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6b5e4-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6b5e4-115">Return code</span></span>                                                                          | <span data-ttu-id="6b5e4-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b5e4-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6b5e4-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6b5e4-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6b5e4-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="6b5e4-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="6b5e4-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b5e4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b5e4-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="6b5e4-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





