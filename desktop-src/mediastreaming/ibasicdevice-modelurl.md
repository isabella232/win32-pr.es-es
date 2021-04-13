---
title: IBasicDevice ModelUrl, método
description: Recupera la dirección URL del modelo del dispositivo.
ms.assetid: 093D306B-5DFC-4A68-803D-3DDE195A8B85
keywords:
- Método ModelUrl API de streaming de multimedia
- Método ModelUrl API de streaming de multimedia, interfaz IBasicDevice
- Interfaz IBasicDevice API de streaming de multimedia, método ModelUrl
topic_type:
- apiref
api_name:
- IBasicDevice.ModelUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f616d1a122f5fe6025c80742df61eb86d41514a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358077"
---
# <a name="ibasicdevicemodelurl-method"></a><span data-ttu-id="9fe3f-106">IBasicDevice:: ModelUrl (método)</span><span class="sxs-lookup"><span data-stu-id="9fe3f-106">IBasicDevice::ModelUrl method</span></span>

<span data-ttu-id="9fe3f-107">Recupera la dirección URL del modelo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-107">Retrieves the device s model URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fe3f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fe3f-108">Syntax</span></span>


```C++
HRESULT ModelUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="9fe3f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9fe3f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fe3f-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9fe3f-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe3f-111">Recibe un puntero a la dirección URL del modelo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-111">Receives a pointer to the device s model URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fe3f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9fe3f-112">Return value</span></span>

<span data-ttu-id="9fe3f-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9fe3f-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9fe3f-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9fe3f-115">Return code</span></span>                                                                          | <span data-ttu-id="9fe3f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fe3f-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9fe3f-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9fe3f-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9fe3f-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="9fe3f-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="9fe3f-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fe3f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fe3f-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="9fe3f-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





