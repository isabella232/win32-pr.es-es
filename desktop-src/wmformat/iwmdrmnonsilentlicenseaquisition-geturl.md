---
title: Método GetURL IWMDRMNonSilentLicenseAquisition (wmdrmsdk. h)
description: El método GetURL recupera la dirección URL a la que se debe publicar el desafío de licencia.
ms.assetid: f65f1984-74bc-4cd0-957e-930aa6a6f6a5
keywords:
- Método GetURL formato de Windows Media
- Método GetURL formato de Windows Media, interfaz IWMDRMNonSilentLicenseAquisition
- Interfaz IWMDRMNonSilentLicenseAquisition formato de Windows Media, método GetURL
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetURL
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79212d19d7dbf4a66e2b72dcbdeba9262a9aeddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679139"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongeturl-method"></a><span data-ttu-id="554c9-106">IWMDRMNonSilentLicenseAquisition:: GetURL (método)</span><span class="sxs-lookup"><span data-stu-id="554c9-106">IWMDRMNonSilentLicenseAquisition::GetURL method</span></span>

<span data-ttu-id="554c9-107">El método **getURL** recupera la dirección URL a la que se debe publicar el desafío de licencia.</span><span class="sxs-lookup"><span data-stu-id="554c9-107">The **GetURL** method retrieves the URL to which the license challenge should be posted.</span></span>

## <a name="syntax"></a><span data-ttu-id="554c9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="554c9-108">Syntax</span></span>


```C++
HRESULT GetURL(
  [out] BSTR *pbstrURL
);
```



## <a name="parameters"></a><span data-ttu-id="554c9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="554c9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="554c9-110">*pbstrURL* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="554c9-110">*pbstrURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="554c9-111">Dirección de una variable que recibe la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="554c9-111">Address of a variable that receives the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="554c9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="554c9-112">Return value</span></span>

<span data-ttu-id="554c9-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="554c9-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="554c9-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="554c9-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="554c9-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="554c9-115">Return code</span></span>                                                                          | <span data-ttu-id="554c9-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="554c9-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="554c9-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="554c9-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="554c9-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="554c9-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="554c9-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="554c9-119">Remarks</span></span>

<span data-ttu-id="554c9-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="554c9-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="554c9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="554c9-121">Requirements</span></span>



| <span data-ttu-id="554c9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="554c9-122">Requirement</span></span> | <span data-ttu-id="554c9-123">Value</span><span class="sxs-lookup"><span data-stu-id="554c9-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="554c9-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="554c9-124">Header</span></span><br/>  | <dl> <span data-ttu-id="554c9-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="554c9-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="554c9-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="554c9-126">Library</span></span><br/> | <dl> <span data-ttu-id="554c9-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="554c9-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="554c9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="554c9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="554c9-129">**Interfaz IWMDRMNonSilentLicenseAquisition**</span><span class="sxs-lookup"><span data-stu-id="554c9-129">**IWMDRMNonSilentLicenseAquisition Interface**</span></span>](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





