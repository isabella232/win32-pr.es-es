---
title: Método IWMDRMLicense PersistLicense (wmdrmsdk. h)
description: El método PersistLicense guarda la licencia actual del almacén temporal en el almacén de licencias local permanente.
ms.assetid: 80a0f932-2800-416b-9dfe-97654a76c19b
keywords:
- Método PersistLicense formato de Windows Media
- Método PersistLicense formato de Windows Media, interfaz IWMDRMLicense
- Interfaz IWMDRMLicense formato de Windows Media, método PersistLicense
topic_type:
- apiref
api_name:
- IWMDRMLicense.PersistLicense
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f41b61cdf448d757d13917ca22af0c3d9d9d390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708820"
---
# <a name="iwmdrmlicensepersistlicense-method"></a><span data-ttu-id="d3e7f-106">IWMDRMLicense::P método ersistLicense</span><span class="sxs-lookup"><span data-stu-id="d3e7f-106">IWMDRMLicense::PersistLicense method</span></span>

<span data-ttu-id="d3e7f-107">El método **PersistLicense** guarda la licencia actual del almacén temporal en el almacén de licencias local permanente.</span><span class="sxs-lookup"><span data-stu-id="d3e7f-107">The **PersistLicense** method saves the current license from the temporary store into the permanent local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3e7f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3e7f-108">Syntax</span></span>


```C++
HRESULT PersistLicense();
```



## <a name="parameters"></a><span data-ttu-id="d3e7f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3e7f-109">Parameters</span></span>

<span data-ttu-id="d3e7f-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d3e7f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3e7f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3e7f-111">Return value</span></span>

<span data-ttu-id="d3e7f-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d3e7f-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d3e7f-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="d3e7f-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d3e7f-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d3e7f-114">Return code</span></span>                                                                          | <span data-ttu-id="d3e7f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3e7f-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d3e7f-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d3e7f-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d3e7f-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="d3e7f-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d3e7f-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3e7f-118">Remarks</span></span>

<span data-ttu-id="d3e7f-119">Si la licencia actual no está en el almacén temporal, se producirá un error en este método.</span><span class="sxs-lookup"><span data-stu-id="d3e7f-119">If the current license is not in the temporary store, this method will fail.</span></span>

<span data-ttu-id="d3e7f-120">Puede llamar a [**CanPersist**](iwmdrmlicense-canpersist.md) para consultar si se permite que se conserve la licencia.</span><span class="sxs-lookup"><span data-stu-id="d3e7f-120">You can call [**CanPersist**](iwmdrmlicense-canpersist.md) to query whether the license is allowed to be persisted.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3e7f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3e7f-121">Requirements</span></span>



| <span data-ttu-id="d3e7f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3e7f-122">Requirement</span></span> | <span data-ttu-id="d3e7f-123">Value</span><span class="sxs-lookup"><span data-stu-id="d3e7f-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e7f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3e7f-124">Header</span></span><br/> | <dl> <span data-ttu-id="d3e7f-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3e7f-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3e7f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3e7f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3e7f-127">**Interfaz IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="d3e7f-127">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





