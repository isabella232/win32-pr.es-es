---
title: IBasicDevice (método de tipo)
description: Recupera un valor de enumeración que indica el tipo de dispositivo del dispositivo DLNA.
ms.assetid: D9FB3A02-7796-4ACB-B7D3-D171D1D9B77F
keywords:
- Método Type API de streaming de multimedia
- Método de tipo API de streaming multimedia, interfaz IBasicDevice
- Interfaz IBasicDevice API de streaming de multimedia, método de tipo
topic_type:
- apiref
api_name:
- IBasicDevice.Type
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a69f0671c82363ff61179c0120b3db8f6e755de9
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "104421596"
---
# <a name="ibasicdevicetype-method"></a><span data-ttu-id="4f242-106">IBasicDevice:: Type (método)</span><span class="sxs-lookup"><span data-stu-id="4f242-106">IBasicDevice::Type method</span></span>

<span data-ttu-id="4f242-107">Recupera un valor de enumeración que indica el tipo de dispositivo del dispositivo DLNA.</span><span class="sxs-lookup"><span data-stu-id="4f242-107">Retrieves an enumeration value indicating the device type of the DLNA device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f242-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f242-108">Syntax</span></span>


```C++
HRESULT Type(
  [out] DeviceTypes *value
);
```



## <a name="parameters"></a><span data-ttu-id="4f242-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f242-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f242-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4f242-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f242-111">Recibe un puntero a un valor de [**DeviceTypes**](devicetypes.md) .</span><span class="sxs-lookup"><span data-stu-id="4f242-111">Receives a pointer to a [**DeviceTypes**](devicetypes.md) value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f242-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f242-112">Return value</span></span>

<span data-ttu-id="4f242-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4f242-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4f242-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="4f242-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4f242-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4f242-115">Return code</span></span>                                                                          | <span data-ttu-id="4f242-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f242-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4f242-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="4f242-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4f242-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="4f242-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="4f242-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f242-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f242-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="4f242-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





