---
title: Método IWMDRMNonSilentLicenseAquisition GetChallenge (wmdrmsdk. h)
description: El método GetChallenge recupera el desafío de la licencia que debe publicarse en el servidor de licencias.
ms.assetid: f2ff8484-8fe2-4c74-82c1-9bc14f8197e0
keywords:
- Método GetChallenge formato de Windows Media
- Método GetChallenge formato de Windows Media, interfaz IWMDRMNonSilentLicenseAquisition
- Interfaz IWMDRMNonSilentLicenseAquisition formato de Windows Media, método GetChallenge
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetChallenge
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa0dc63c63e5d7a62c06cbe791d9a5e5e8d09c5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679483"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongetchallenge-method"></a><span data-ttu-id="67748-106">IWMDRMNonSilentLicenseAquisition:: GetChallenge (método)</span><span class="sxs-lookup"><span data-stu-id="67748-106">IWMDRMNonSilentLicenseAquisition::GetChallenge method</span></span>

<span data-ttu-id="67748-107">El método **GetChallenge** recupera el desafío de la licencia que debe publicarse en el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="67748-107">The **GetChallenge** method retrieves the license challenge that should be posted to the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="67748-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67748-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [out] BSTR *pbstrChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="67748-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67748-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67748-110">*pbstrChallenge* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="67748-110">*pbstrChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67748-111">Dirección de una variable que recibe el desafío de licencia.</span><span class="sxs-lookup"><span data-stu-id="67748-111">Address of a variable that receives the license challenge.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67748-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67748-112">Return value</span></span>

<span data-ttu-id="67748-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="67748-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="67748-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="67748-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="67748-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="67748-115">Return code</span></span>                                                                          | <span data-ttu-id="67748-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="67748-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="67748-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="67748-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="67748-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="67748-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="67748-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67748-119">Remarks</span></span>

<span data-ttu-id="67748-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="67748-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="67748-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67748-121">Requirements</span></span>



| <span data-ttu-id="67748-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="67748-122">Requirement</span></span> | <span data-ttu-id="67748-123">Value</span><span class="sxs-lookup"><span data-stu-id="67748-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67748-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67748-124">Header</span></span><br/>  | <dl> <span data-ttu-id="67748-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="67748-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="67748-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="67748-126">Library</span></span><br/> | <dl> <span data-ttu-id="67748-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67748-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67748-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="67748-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67748-129">**Interfaz IWMDRMNonSilentLicenseAquisition**</span><span class="sxs-lookup"><span data-stu-id="67748-129">**IWMDRMNonSilentLicenseAquisition Interface**</span></span>](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





