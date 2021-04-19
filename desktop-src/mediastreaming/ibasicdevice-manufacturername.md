---
title: IBasicDevice ManufacturerName, método
description: Recupera el nombre del fabricante del dispositivo.
ms.assetid: F04400C9-02FC-4CB5-B355-A7E84BECD098
keywords:
- Método ManufacturerName API de streaming de multimedia
- Método ManufacturerName API de streaming de multimedia, interfaz IBasicDevice
- Interfaz IBasicDevice API de streaming de multimedia, método ManufacturerName
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 698b4b6c202ed157737b20296976a282c7f97ba3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105695510"
---
# <a name="ibasicdevicemanufacturername-method"></a><span data-ttu-id="20a97-106">IBasicDevice:: ManufacturerName (método)</span><span class="sxs-lookup"><span data-stu-id="20a97-106">IBasicDevice::ManufacturerName method</span></span>

<span data-ttu-id="20a97-107">Recupera el nombre del fabricante del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20a97-107">Retrieves the device s manufacturer name.</span></span>

## <a name="syntax"></a><span data-ttu-id="20a97-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20a97-108">Syntax</span></span>


```C++
HRESULT ManufacturerName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="20a97-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20a97-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20a97-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="20a97-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20a97-111">Recibe un puntero al nombre del fabricante del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20a97-111">Receives a pointer to the device s manufacturer name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20a97-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20a97-112">Return value</span></span>

<span data-ttu-id="20a97-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="20a97-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="20a97-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="20a97-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="20a97-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="20a97-115">Return code</span></span>                                                                          | <span data-ttu-id="20a97-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="20a97-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="20a97-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="20a97-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="20a97-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="20a97-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="20a97-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="20a97-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20a97-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="20a97-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





