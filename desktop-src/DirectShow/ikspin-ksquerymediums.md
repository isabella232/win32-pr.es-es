---
description: El método KsQueryMediums recupera los medios admitidos por un PIN.
ms.assetid: 554bf968-6054-4f9d-95db-facf0444641f
title: 'IKsPin:: KsQueryMediums (método) (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin.KsQueryMediums
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: f037317b49bc54f5ea9db5b7a4ae039ec0a9970d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806080"
---
# <a name="ikspinksquerymediums-method"></a><span data-ttu-id="c62b2-103">IKsPin:: KsQueryMediums (método)</span><span class="sxs-lookup"><span data-stu-id="c62b2-103">IKsPin::KsQueryMediums method</span></span>

<span data-ttu-id="c62b2-104">El `KsQueryMediums` método recupera los medios admitidos por un PIN.</span><span class="sxs-lookup"><span data-stu-id="c62b2-104">The `KsQueryMediums` method retrieves the mediums supported by a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="c62b2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c62b2-105">Syntax</span></span>


```C++
HRESULT KsQueryMediums(
  [out] KSMULTIPLE_ITEM **ppmi
);
```



## <a name="parameters"></a><span data-ttu-id="c62b2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c62b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c62b2-107">*PPMI* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c62b2-107">*ppmi* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c62b2-108">Dirección de un puntero a una estructura de [**\_ elementos KSMULTIPLE**](ksmultiple-item.md) .</span><span class="sxs-lookup"><span data-stu-id="c62b2-108">Address of a pointer to a [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c62b2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c62b2-109">Return value</span></span>

<span data-ttu-id="c62b2-110">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="c62b2-110">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="c62b2-111">Si se produce un error, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c62b2-111">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c62b2-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c62b2-112">Remarks</span></span>

<span data-ttu-id="c62b2-113">Este método devuelve una estructura de [**\_ elemento KSMULTIPLE**](ksmultiple-item.md) asignada por la tarea, seguida de cero o más estructuras [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) .</span><span class="sxs-lookup"><span data-stu-id="c62b2-113">This method returns a task-allocated [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure, which is followed by zero or more [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) structures.</span></span> <span data-ttu-id="c62b2-114">El miembro **Count** de la estructura del **\_ elemento KSMULTIPLE** especifica el número de estructuras **REGPINMEDIUM** .</span><span class="sxs-lookup"><span data-stu-id="c62b2-114">The **Count** member of the **KSMULTIPLE\_ITEM** structure specifies the number of **REGPINMEDIUM** structures.</span></span> <span data-ttu-id="c62b2-115">Cada estructura **REGPINMEDIUM** define un medio admitido por el PIN.</span><span class="sxs-lookup"><span data-stu-id="c62b2-115">Each **REGPINMEDIUM** structure defines a medium supported by the pin.</span></span>

<span data-ttu-id="c62b2-116">El llamador debe liberar las estructuras devueltas mediante la función **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="c62b2-116">The caller must free the returned structures, using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="c62b2-117">Debe incluir KS. h antes de ksproxy. h.</span><span class="sxs-lookup"><span data-stu-id="c62b2-117">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="examples"></a><span data-ttu-id="c62b2-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c62b2-118">Examples</span></span>

<span data-ttu-id="c62b2-119">La siguiente función auxiliar intenta hacer coincidir un pin con un medio especificado.</span><span class="sxs-lookup"><span data-stu-id="c62b2-119">The following helper function attempts to match a pin against a specified medium.</span></span>


```C++
HRESULT FindMatchingMedium(
    IPin *pPin, 
    REGPINMEDIUM *pMedium, 
    bool *pfMatch)
{
    IKsPin* pKsPin = NULL;
    KSMULTIPLE_ITEM *pmi;

    *pfMatch = false;
    HRESULT hr = pPin->QueryInterface(IID_IKsPin, (void **)&pKsPin);
    if (FAILED(hr)) 
        return hr;  // Pin does not support IKsPin.

    hr = pKsPin->KsQueryMediums(&pmi);
    pKsPin->Release();
    if (FAILED(hr))
        return hr;  // Pin does not support mediums.

    if (pmi->Count) 
    {
        // Use pointer arithmetic to reference the first medium structure.
        REGPINMEDIUM *pTemp = (REGPINMEDIUM*)(pmi + 1);
        for (ULONG i = 0; i < pmi->Count; i++, pTemp++) 
        {
            if (pMedium->clsMedium == pTemp->clsMedium) 
            {
                *pfMatch = true;
                break;
            }
        }
    }        
    CoTaskMemFree(pmi);
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="c62b2-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c62b2-120">Requirements</span></span>



| <span data-ttu-id="c62b2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c62b2-121">Requirement</span></span> | <span data-ttu-id="c62b2-122">Value</span><span class="sxs-lookup"><span data-stu-id="c62b2-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c62b2-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c62b2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c62b2-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c62b2-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c62b2-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c62b2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c62b2-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c62b2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c62b2-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c62b2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c62b2-128"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="c62b2-128"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="c62b2-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c62b2-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="c62b2-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c62b2-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c62b2-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="c62b2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c62b2-132">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="c62b2-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="c62b2-133">**Interfaz IKsPin**</span><span class="sxs-lookup"><span data-stu-id="c62b2-133">**IKsPin Interface**</span></span>](ikspin.md)
</dt> <dt>

[<span data-ttu-id="c62b2-134">Filtros de controlador de clase WDM</span><span class="sxs-lookup"><span data-stu-id="c62b2-134">WDM Class Driver Filters</span></span>](wdm-class-driver-filters.md)
</dt> </dl>

 

 




