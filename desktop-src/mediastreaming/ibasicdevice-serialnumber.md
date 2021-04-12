---
title: IBasicDevice SerialNumber (método)
description: Recupera el número de serie del dispositivo.
ms.assetid: 238A5999-0E8B-4462-AFCF-790DB58CFCB4
keywords:
- Método SerialNumber API de streaming de multimedia
- Método SerialNumber API de streaming de multimedia, interfaz IBasicDevice
- Interfaz IBasicDevice streaming de multimedia API, método SerialNumber
topic_type:
- apiref
api_name:
- IBasicDevice.SerialNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f24fad2e74c3ec2a5b489d8f5dd57265ea6d21bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358089"
---
# <a name="ibasicdeviceserialnumber-method"></a><span data-ttu-id="22936-106">IBasicDevice:: SerialNumber (método)</span><span class="sxs-lookup"><span data-stu-id="22936-106">IBasicDevice::SerialNumber method</span></span>

<span data-ttu-id="22936-107">Recupera el número de serie del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22936-107">Retrieves the device s serial number.</span></span>

## <a name="syntax"></a><span data-ttu-id="22936-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22936-108">Syntax</span></span>


```C++
HRESULT SerialNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="22936-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22936-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22936-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="22936-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22936-111">Recibe un puntero al número de serie del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22936-111">Receives a pointer to the device s serial number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22936-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22936-112">Return value</span></span>

<span data-ttu-id="22936-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="22936-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="22936-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="22936-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="22936-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="22936-115">Return code</span></span>                                                                          | <span data-ttu-id="22936-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="22936-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="22936-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="22936-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="22936-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="22936-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="22936-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="22936-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22936-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="22936-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





