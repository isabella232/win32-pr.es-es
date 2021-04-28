---
description: 'Método CPosPassThru.IsFormatSupported: el método IsFormatSupported determina si se admite un formato de hora especificado. Este método implementa el método IMediaSeeking::IsFormatSupported.'
ms.assetid: dd8751d6-8439-4155-bdaf-b152a7c6cad4
title: Método CPosPassThru.IsFormatSupported (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bd4b90bbe86e7ba05aa48fb7888c946babd8ed9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095253"
---
# <a name="cpospassthruisformatsupported-method"></a><span data-ttu-id="67075-104">Método CPosPassThru.IsFormatSupported</span><span class="sxs-lookup"><span data-stu-id="67075-104">CPosPassThru.IsFormatSupported method</span></span>

<span data-ttu-id="67075-105">El `IsFormatSupported` método determina si se admite un formato de hora especificado.</span><span class="sxs-lookup"><span data-stu-id="67075-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="67075-106">Este método implementa el [**método IMediaSeeking::IsFormatSupported.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported)</span><span class="sxs-lookup"><span data-stu-id="67075-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="67075-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67075-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="67075-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67075-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67075-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="67075-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="67075-110">Puntero a un GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="67075-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67075-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67075-111">Return value</span></span>

<span data-ttu-id="67075-112">Devuelve el **valor HRESULT** del pin conectado.</span><span class="sxs-lookup"><span data-stu-id="67075-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="67075-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67075-113">Requirements</span></span>



| <span data-ttu-id="67075-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="67075-114">Requirement</span></span> | <span data-ttu-id="67075-115">Value</span><span class="sxs-lookup"><span data-stu-id="67075-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67075-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67075-116">Header</span></span><br/>  | <dl> <span data-ttu-id="67075-117"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="67075-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="67075-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="67075-118">Library</span></span><br/> | <dl> <span data-ttu-id="67075-119"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="67075-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67075-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="67075-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67075-121">**CPosPassThru (clase)**</span><span class="sxs-lookup"><span data-stu-id="67075-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="67075-122">**GUID de formato de hora**</span><span class="sxs-lookup"><span data-stu-id="67075-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




