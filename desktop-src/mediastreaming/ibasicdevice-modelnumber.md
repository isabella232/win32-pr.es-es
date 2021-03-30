---
title: IBasicDevice ModelNumber, método
description: Recupera el número de modelo del dispositivo.
ms.assetid: C4199135-0C6C-4427-8152-224D7D29C270
keywords:
- Método ModelNumber API de streaming de multimedia
- Método ModelNumber API de streaming de multimedia, interfaz IBasicDevice
- Interfaz IBasicDevice API de streaming de multimedia, método ModelNumber
topic_type:
- apiref
api_name:
- IBasicDevice.ModelNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8034e67e5f3c552f0af83678d75e33881f1318f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904069"
---
# <a name="ibasicdevicemodelnumber-method"></a><span data-ttu-id="223b8-106">IBasicDevice:: ModelNumber (método)</span><span class="sxs-lookup"><span data-stu-id="223b8-106">IBasicDevice::ModelNumber method</span></span>

<span data-ttu-id="223b8-107">Recupera el número de modelo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="223b8-107">Retrieves the device s model number.</span></span>

## <a name="syntax"></a><span data-ttu-id="223b8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="223b8-108">Syntax</span></span>


```C++
HRESULT ModelNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="223b8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="223b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="223b8-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="223b8-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="223b8-111">Recibe un puntero al número de modelo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="223b8-111">Receives a pointer to the device s model number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="223b8-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="223b8-112">Return value</span></span>

<span data-ttu-id="223b8-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="223b8-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="223b8-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="223b8-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="223b8-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="223b8-115">Return code</span></span>                                                                          | <span data-ttu-id="223b8-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="223b8-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="223b8-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="223b8-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="223b8-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="223b8-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="223b8-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="223b8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="223b8-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="223b8-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





