---
title: Método IWMDRMLicense ResetEnumeration (wmdrmsdk. h)
description: El método ResetEnumeration restablece la lista de licencias a su estado original. La licencia activa se convierte en la primera licencia de la lista.
ms.assetid: cb5a31a8-ee25-44d6-81ca-746c379cb99e
keywords:
- Método ResetEnumeration formato de Windows Media
- Método ResetEnumeration formato de Windows Media, interfaz IWMDRMLicense
- Interfaz IWMDRMLicense formato de Windows Media, método ResetEnumeration
topic_type:
- apiref
api_name:
- IWMDRMLicense.ResetEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6510c05b4c974051d9902ed2d30d9cdf99956af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708710"
---
# <a name="iwmdrmlicenseresetenumeration-method"></a><span data-ttu-id="8819b-107">IWMDRMLicense:: ResetEnumeration (método)</span><span class="sxs-lookup"><span data-stu-id="8819b-107">IWMDRMLicense::ResetEnumeration method</span></span>

<span data-ttu-id="8819b-108">El método **ResetEnumeration** restablece la lista de licencias a su estado original.</span><span class="sxs-lookup"><span data-stu-id="8819b-108">The **ResetEnumeration** method resets the license list to its original state.</span></span> <span data-ttu-id="8819b-109">La licencia activa se convierte en la primera licencia de la lista.</span><span class="sxs-lookup"><span data-stu-id="8819b-109">The active license becomes the first license in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="8819b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8819b-110">Syntax</span></span>


```C++
HRESULT ResetEnumeration();
```



## <a name="parameters"></a><span data-ttu-id="8819b-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8819b-111">Parameters</span></span>

<span data-ttu-id="8819b-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8819b-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8819b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8819b-113">Return value</span></span>

<span data-ttu-id="8819b-114">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8819b-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8819b-115">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="8819b-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8819b-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8819b-116">Return code</span></span>                                                                                                | <span data-ttu-id="8819b-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="8819b-117">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="8819b-118"><dt>**NS \_ E \_ DRM \_ RIV \_ demasiado \_ pequeño**</dt></span><span class="sxs-lookup"><span data-stu-id="8819b-118"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="8819b-119">Se necesita una lista de revocación de contenido actualizada.</span><span class="sxs-lookup"><span data-stu-id="8819b-119">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="8819b-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8819b-120"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="8819b-121">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="8819b-121">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="8819b-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8819b-122">Remarks</span></span>

<span data-ttu-id="8819b-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8819b-123">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="8819b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8819b-124">Requirements</span></span>



| <span data-ttu-id="8819b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8819b-125">Requirement</span></span> | <span data-ttu-id="8819b-126">Value</span><span class="sxs-lookup"><span data-stu-id="8819b-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8819b-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8819b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="8819b-128"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="8819b-128"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="8819b-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8819b-129">Library</span></span><br/> | <dl> <span data-ttu-id="8819b-130"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8819b-130"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8819b-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="8819b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8819b-132">**Interfaz IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="8819b-132">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





