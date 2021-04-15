---
description: Método de constructor.
ms.assetid: b258401c-158b-4eb8-8736-1e1ad9a8403a
title: Constructor CPosPassThru. CPosPassThru
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CPosPassThru
api_type:
- COM
api_location: ''
ms.openlocfilehash: ba49bd1e2f65cf0d2a8a398ecab167e74dc35ad4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677059"
---
# <a name="cpospassthrucpospassthru-constructor"></a><span data-ttu-id="2e2f0-103">Constructor CPosPassThru. CPosPassThru</span><span class="sxs-lookup"><span data-stu-id="2e2f0-103">CPosPassThru.CPosPassThru constructor</span></span>

<span data-ttu-id="2e2f0-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="2e2f0-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e2f0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e2f0-105">Syntax</span></span>


```C++
CPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin,
                   
);
```



## <a name="parameters"></a><span data-ttu-id="2e2f0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e2f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e2f0-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="2e2f0-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="2e2f0-108">Puntero al nombre del objeto, para la depuración.</span><span class="sxs-lookup"><span data-stu-id="2e2f0-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="2e2f0-109">Asigne este parámetro en la memoria estática.</span><span class="sxs-lookup"><span data-stu-id="2e2f0-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="2e2f0-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="2e2f0-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="2e2f0-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="2e2f0-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="2e2f0-112">Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="2e2f0-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="2e2f0-113">De lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="2e2f0-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2e2f0-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="2e2f0-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="2e2f0-115">Puntero a un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2e2f0-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="2e2f0-116">ignorado.</span><span class="sxs-lookup"><span data-stu-id="2e2f0-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="2e2f0-117">*pPin*</span><span class="sxs-lookup"><span data-stu-id="2e2f0-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="2e2f0-118">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN de entrada del filtro.</span><span class="sxs-lookup"><span data-stu-id="2e2f0-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> <dt>

 
</dt> <dd></dd> </dl>

 

 



