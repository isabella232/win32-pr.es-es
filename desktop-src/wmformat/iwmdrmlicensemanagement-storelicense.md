---
title: Método IWMDRMLicenseManagement StoreLicense (wmdrmsdk. h)
description: El método StoreLicense incluye una licencia que se generó fuera del subsistema DRM local en el almacén de licencias local.
ms.assetid: 2190ff8c-8969-4f03-9f90-331bff8f4da2
keywords:
- Método StoreLicense formato de Windows Media
- Método StoreLicense formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método StoreLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.StoreLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcfde6347e099ceb9fc168e1183cbd62c90f9b9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718673"
---
# <a name="iwmdrmlicensemanagementstorelicense-method"></a><span data-ttu-id="1158d-106">IWMDRMLicenseManagement:: StoreLicense (método)</span><span class="sxs-lookup"><span data-stu-id="1158d-106">IWMDRMLicenseManagement::StoreLicense method</span></span>

<span data-ttu-id="1158d-107">El método **StoreLicense** incluye una licencia que se generó fuera del subsistema DRM local en el almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="1158d-107">The **StoreLicense** method includes a license that was generated outside of the local DRM subsystem in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="1158d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1158d-108">Syntax</span></span>


```C++
HRESULT StoreLicense(
  [in] BSTR bstrLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="1158d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1158d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1158d-110">*bstrLicenseResponse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1158d-110">*bstrLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1158d-111">Cadena de respuesta de licencia que se va a descodificar y agregar al almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="1158d-111">License response string to be decoded and added to the local license store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1158d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1158d-112">Return value</span></span>

<span data-ttu-id="1158d-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1158d-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1158d-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="1158d-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1158d-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1158d-115">Return code</span></span>                                                                          | <span data-ttu-id="1158d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="1158d-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1158d-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1158d-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1158d-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="1158d-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1158d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1158d-119">Remarks</span></span>

<span data-ttu-id="1158d-120">Puede usar este método para agregar licencias de XMR que haya creado al almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="1158d-120">You can use this method to add XMR licenses that you have created to the local license store.</span></span>

## <a name="requirements"></a><span data-ttu-id="1158d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1158d-121">Requirements</span></span>



| <span data-ttu-id="1158d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1158d-122">Requirement</span></span> | <span data-ttu-id="1158d-123">Value</span><span class="sxs-lookup"><span data-stu-id="1158d-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1158d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1158d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1158d-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="1158d-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="1158d-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1158d-126">Library</span></span><br/> | <dl> <span data-ttu-id="1158d-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1158d-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1158d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="1158d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1158d-129">**Interfaz IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="1158d-129">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





