---
title: IBasicDevice IpAddresses, método
description: Devuelve un vector de direcciones IP.
ms.assetid: F48B91DC-3AE2-462F-835B-292BF86904B3
keywords:
- Método IpAddresses API de streaming de multimedia
- Método IpAddresses API de streaming de multimedia, interfaz IBasicDevice
- Interfaz IBasicDevice API de streaming de multimedia, método IpAddresses
topic_type:
- apiref
api_name:
- IBasicDevice.IpAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0623b6e2e5d96cb0a400ab1e820424b7eecf46c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419524"
---
# <a name="ibasicdeviceipaddresses-method"></a><span data-ttu-id="02a09-106">IBasicDevice:: IpAddresses (método)</span><span class="sxs-lookup"><span data-stu-id="02a09-106">IBasicDevice::IpAddresses method</span></span>

<span data-ttu-id="02a09-107">Devuelve un vector de direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="02a09-107">Returns a vector of IP addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="02a09-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02a09-108">Syntax</span></span>


```C++
HRESULT IpAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a><span data-ttu-id="02a09-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02a09-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02a09-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="02a09-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02a09-111">Recibe una colección enumerable de punteros a direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="02a09-111">Receives an enumerable collection of pointers to IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02a09-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02a09-112">Return value</span></span>

<span data-ttu-id="02a09-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="02a09-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="02a09-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="02a09-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="02a09-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="02a09-115">Return code</span></span>                                                                          | <span data-ttu-id="02a09-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="02a09-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="02a09-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="02a09-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="02a09-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="02a09-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="02a09-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="02a09-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02a09-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="02a09-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





