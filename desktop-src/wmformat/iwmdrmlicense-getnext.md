---
title: Método GetNext IWMDRMLicense (wmdrmsdk. h)
description: El método GetNext carga la información sobre el elemento siguiente de la lista.
ms.assetid: 5ef91751-2883-4a8e-9908-7a6dfe6d2af3
keywords:
- Método GetNext formato de Windows Media
- Método GetNext formato de Windows Media, interfaz IWMDRMLicense
- Interfaz IWMDRMLicense formato de Windows Media, método GetNext
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetNext
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da1dd1f8ce41648c7a67730d909058d10d616e7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708648"
---
# <a name="iwmdrmlicensegetnext-method"></a><span data-ttu-id="dcb57-106">IWMDRMLicense:: GetNext (método)</span><span class="sxs-lookup"><span data-stu-id="dcb57-106">IWMDRMLicense::GetNext method</span></span>

<span data-ttu-id="dcb57-107">El método **Getnext** carga la información sobre el elemento siguiente de la lista.</span><span class="sxs-lookup"><span data-stu-id="dcb57-107">The **GetNext** method loads the information about the next item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcb57-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dcb57-108">Syntax</span></span>


```C++
HRESULT GetNext();
```



## <a name="parameters"></a><span data-ttu-id="dcb57-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dcb57-109">Parameters</span></span>

<span data-ttu-id="dcb57-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="dcb57-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dcb57-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dcb57-111">Return value</span></span>

<span data-ttu-id="dcb57-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="dcb57-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="dcb57-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="dcb57-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="dcb57-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="dcb57-114">Return code</span></span>                                                                                                | <span data-ttu-id="dcb57-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="dcb57-115">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="dcb57-116"><dt>**NS \_ E \_ DRM \_ RIV \_ demasiado \_ pequeño**</dt></span><span class="sxs-lookup"><span data-stu-id="dcb57-116"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="dcb57-117">Se necesita una lista de revocación de contenido actualizada.</span><span class="sxs-lookup"><span data-stu-id="dcb57-117">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="dcb57-118"><dt>**\_no hay \_ más \_ elementos de error**</dt></span><span class="sxs-lookup"><span data-stu-id="dcb57-118"><dt>**ERROR\_NO\_MORE\_ITEMS**</dt></span></span> </dl>      | <span data-ttu-id="dcb57-119">En la lista no hay más elementos.</span><span class="sxs-lookup"><span data-stu-id="dcb57-119">There are no more items in the list.</span></span><br/>          |
| <dl> <span data-ttu-id="dcb57-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="dcb57-120"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="dcb57-121">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="dcb57-121">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="dcb57-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dcb57-122">Remarks</span></span>

<span data-ttu-id="dcb57-123">Los métodos de la interfaz [**IWMDRMLicense**](iwmdrmlicense.md) proporcionan datos sobre una sola licencia a la vez.</span><span class="sxs-lookup"><span data-stu-id="dcb57-123">The methods of the [**IWMDRMLicense**](iwmdrmlicense.md) interface provide data about a single license at a time.</span></span> <span data-ttu-id="dcb57-124">El objeto subyacente contiene una lista de una o más licencias.</span><span class="sxs-lookup"><span data-stu-id="dcb57-124">The underlying object contains a list of one or more licenses.</span></span> <span data-ttu-id="dcb57-125">Cuando se llama a este método, la interfaz mueve sus referencias internas a la siguiente licencia de la lista.</span><span class="sxs-lookup"><span data-stu-id="dcb57-125">When you call this method, the interface moves its internal references to the next license in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcb57-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcb57-126">Requirements</span></span>



| <span data-ttu-id="dcb57-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcb57-127">Requirement</span></span> | <span data-ttu-id="dcb57-128">Value</span><span class="sxs-lookup"><span data-stu-id="dcb57-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcb57-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dcb57-129">Header</span></span><br/>  | <dl> <span data-ttu-id="dcb57-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcb57-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="dcb57-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dcb57-131">Library</span></span><br/> | <dl> <span data-ttu-id="dcb57-132"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcb57-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcb57-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="dcb57-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcb57-134">**Interfaz IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="dcb57-134">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





