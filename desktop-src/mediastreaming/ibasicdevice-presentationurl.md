---
title: IBasicDevice PresentationUrl, método
description: Recupera la dirección URL de presentación del dispositivo.
ms.assetid: F1EF1BBE-F35D-4828-B4F6-D6DEFF5A6391
keywords:
- Método PresentationUrl API de streaming de multimedia
- Método PresentationUrl API de streaming de multimedia, interfaz IBasicDevice
- Interfaz IBasicDevice API de streaming de multimedia, método PresentationUrl
topic_type:
- apiref
api_name:
- IBasicDevice.PresentationUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89d10187329692c4f279a94cde004455a182733e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419512"
---
# <a name="ibasicdevicepresentationurl-method"></a><span data-ttu-id="f467e-106">IBasicDevice::P método resentationUrl</span><span class="sxs-lookup"><span data-stu-id="f467e-106">IBasicDevice::PresentationUrl method</span></span>

<span data-ttu-id="f467e-107">Recupera la dirección URL de presentación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f467e-107">Retrieves the device s presentation URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="f467e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f467e-108">Syntax</span></span>


```C++
HRESULT PresentationUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="f467e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f467e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f467e-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f467e-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f467e-111">Recibe un puntero a la dirección URL de presentación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f467e-111">Receives a pointer to the device s presentation URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f467e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f467e-112">Return value</span></span>

<span data-ttu-id="f467e-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f467e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f467e-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="f467e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f467e-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f467e-115">Return code</span></span>                                                                          | <span data-ttu-id="f467e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="f467e-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f467e-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f467e-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f467e-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="f467e-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="f467e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="f467e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f467e-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="f467e-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





