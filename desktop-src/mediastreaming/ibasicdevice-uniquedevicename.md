---
title: IBasicDevice UniqueDeviceName, método
description: Recupera el nombre del dispositivo único (UDN).
ms.assetid: 393EFF96-69E1-4081-905D-D8CC47B5FC4A
keywords:
- Método UniqueDeviceName API de streaming de multimedia
- Método UniqueDeviceName API de streaming de multimedia, interfaz IBasicDevice
- Interfaz IBasicDevice API de streaming de multimedia, método UniqueDeviceName
topic_type:
- apiref
api_name:
- IBasicDevice.UniqueDeviceName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4b3103640fd49880dc5ae5ca881618ac1091de62
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419500"
---
# <a name="ibasicdeviceuniquedevicename-method"></a><span data-ttu-id="0c286-106">IBasicDevice:: UniqueDeviceName (método)</span><span class="sxs-lookup"><span data-stu-id="0c286-106">IBasicDevice::UniqueDeviceName method</span></span>

<span data-ttu-id="0c286-107">Recupera el nombre del dispositivo único (UDN).</span><span class="sxs-lookup"><span data-stu-id="0c286-107">Retrieves the device s unique device name (UDN).</span></span>

## <a name="syntax"></a><span data-ttu-id="0c286-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c286-108">Syntax</span></span>


```C++
HRESULT UniqueDeviceName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="0c286-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c286-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c286-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0c286-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c286-111">Recibe un puntero a la UDN del modelo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c286-111">Receives a pointer to the device s model UDN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c286-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c286-112">Return value</span></span>

<span data-ttu-id="0c286-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0c286-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0c286-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="0c286-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0c286-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0c286-115">Return code</span></span>                                                                          | <span data-ttu-id="0c286-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c286-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0c286-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0c286-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0c286-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="0c286-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="0c286-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c286-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c286-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="0c286-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





