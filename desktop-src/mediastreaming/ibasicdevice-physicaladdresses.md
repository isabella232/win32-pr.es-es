---
title: IBasicDevice PhysicalAddresses, método
description: Devuelve un vector de direcciones físicas.
ms.assetid: 85F48EE3-14A1-46DA-A3C3-F94A8A43CF92
keywords:
- Método PhysicalAddresses API de streaming de multimedia
- Método PhysicalAddresses API de streaming de multimedia, interfaz IBasicDevice
- Interfaz IBasicDevice API de streaming de multimedia, método PhysicalAddresses
topic_type:
- apiref
api_name:
- IBasicDevice.PhysicalAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f1cd87435c78e1f6877d1bb6afd1b38981b05dc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358076"
---
# <a name="ibasicdevicephysicaladdresses-method"></a><span data-ttu-id="2dc5f-106">IBasicDevice::P método hysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="2dc5f-106">IBasicDevice::PhysicalAddresses method</span></span>

<span data-ttu-id="2dc5f-107">Devuelve un vector de direcciones físicas.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-107">Returns a vector of physical addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dc5f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2dc5f-108">Syntax</span></span>


```C++
HRESULT PhysicalAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a><span data-ttu-id="2dc5f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2dc5f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dc5f-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2dc5f-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2dc5f-111">Recibe una colección enumerable de punteros a direcciones físicas.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-111">Receives an enumerable collection of pointers to physical addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dc5f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2dc5f-112">Return value</span></span>

<span data-ttu-id="2dc5f-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2dc5f-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2dc5f-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2dc5f-115">Return code</span></span>                                                                          | <span data-ttu-id="2dc5f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="2dc5f-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2dc5f-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2dc5f-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2dc5f-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="2dc5f-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="2dc5f-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="2dc5f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dc5f-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="2dc5f-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





