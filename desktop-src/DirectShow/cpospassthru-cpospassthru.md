---
description: 'Constructor CPosPassThru.CPosPassThru: método constructor.'
ms.assetid: b258401c-158b-4eb8-8736-1e1ad9a8403a
title: Constructor CPosPassThru.CPosPassThru
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
ms.openlocfilehash: 2a6c49b305b3c6638aeaaee1480d0b561fd8c99a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085603"
---
# <a name="cpospassthrucpospassthru-constructor"></a><span data-ttu-id="a1e53-103">Constructor CPosPassThru.CPosPassThru</span><span class="sxs-lookup"><span data-stu-id="a1e53-103">CPosPassThru.CPosPassThru constructor</span></span>

<span data-ttu-id="a1e53-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="a1e53-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1e53-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1e53-105">Syntax</span></span>


```C++
CPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin,
                   
);
```



## <a name="parameters"></a><span data-ttu-id="a1e53-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1e53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1e53-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="a1e53-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="a1e53-108">Puntero al nombre del objeto para fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="a1e53-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="a1e53-109">Asigne este parámetro en memoria estática.</span><span class="sxs-lookup"><span data-stu-id="a1e53-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="a1e53-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="a1e53-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="a1e53-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="a1e53-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="a1e53-112">Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="a1e53-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="a1e53-113">De lo contrario, establezca este parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="a1e53-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a1e53-114">*Phr*</span><span class="sxs-lookup"><span data-stu-id="a1e53-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="a1e53-115">Puntero a un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="a1e53-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="a1e53-116">ignorado.</span><span class="sxs-lookup"><span data-stu-id="a1e53-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="a1e53-117">*pPin*</span><span class="sxs-lookup"><span data-stu-id="a1e53-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="a1e53-118">Puntero a la [**interfaz IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin de entrada del filtro.</span><span class="sxs-lookup"><span data-stu-id="a1e53-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> <dt>

 
</dt> <dd></dd> </dl>

 

 



