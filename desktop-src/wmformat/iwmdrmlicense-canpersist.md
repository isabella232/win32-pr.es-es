---
title: Método IWMDRMLicense CanPersist (wmdrmsdk. h)
description: El método CanPersist consulta si la licencia puede conservarse en un almacén de licencias local.
ms.assetid: 040b30d8-4e47-44a3-8b09-e81cc30e8a53
keywords:
- Método CanPersist formato de Windows Media
- Método CanPersist formato de Windows Media, interfaz IWMDRMLicense
- Interfaz IWMDRMLicense formato de Windows Media, método CanPersist
topic_type:
- apiref
api_name:
- IWMDRMLicense.CanPersist
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7772dac73b99443626b1eeec6f5e90851f92c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708896"
---
# <a name="iwmdrmlicensecanpersist-method"></a><span data-ttu-id="bb26f-106">IWMDRMLicense:: CanPersist (método)</span><span class="sxs-lookup"><span data-stu-id="bb26f-106">IWMDRMLicense::CanPersist method</span></span>

<span data-ttu-id="bb26f-107">El método **CanPersist** consulta si la licencia puede conservarse en un almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="bb26f-107">The **CanPersist** method queries whether the license can be persisted on in a local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb26f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb26f-108">Syntax</span></span>


```C++
HRESULT CanPersist(
  [out] BOOL *pfCanPersist
);
```



## <a name="parameters"></a><span data-ttu-id="bb26f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb26f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb26f-110">*pfCanPersist* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bb26f-110">*pfCanPersist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb26f-111">TRUE indica que la licencia puede conservarse.</span><span class="sxs-lookup"><span data-stu-id="bb26f-111">TRUE indicates that the license can be persisted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb26f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb26f-112">Return value</span></span>

<span data-ttu-id="bb26f-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="bb26f-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bb26f-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="bb26f-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bb26f-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bb26f-115">Return code</span></span>                                                                          | <span data-ttu-id="bb26f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb26f-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bb26f-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="bb26f-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="bb26f-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="bb26f-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bb26f-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb26f-119">Remarks</span></span>

<span data-ttu-id="bb26f-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bb26f-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb26f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb26f-121">Requirements</span></span>



| <span data-ttu-id="bb26f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb26f-122">Requirement</span></span> | <span data-ttu-id="bb26f-123">Value</span><span class="sxs-lookup"><span data-stu-id="bb26f-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb26f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb26f-124">Header</span></span><br/> | <dl> <span data-ttu-id="bb26f-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb26f-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb26f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb26f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb26f-127">**Interfaz IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="bb26f-127">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





