---
description: Se produce cuando el lápiz deja el intervalo de detección física (proximidad) de la tableta.
ms.assetid: ded01278-126d-415d-9a7b-1e6fe3650a37
title: 'ITabletEventSink:: CursorOutOfRange (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorOutOfRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: e2250401f3888bd07ff250549c11c34e6a54576d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913297"
---
# <a name="itableteventsinkcursoroutofrange-method"></a><span data-ttu-id="7759b-103">ITabletEventSink:: CursorOutOfRange (método)</span><span class="sxs-lookup"><span data-stu-id="7759b-103">ITabletEventSink::CursorOutOfRange method</span></span>

<span data-ttu-id="7759b-104">Se produce cuando el lápiz deja el intervalo de detección física (proximidad) de la tableta.</span><span class="sxs-lookup"><span data-stu-id="7759b-104">Occurs when the stylus leaves the physical detection range (proximity) of the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="7759b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7759b-105">Syntax</span></span>


```C++
HRESULT CursorOutOfRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="7759b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7759b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7759b-107">*TCID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7759b-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7759b-108">El identificador de la tableta.</span><span class="sxs-lookup"><span data-stu-id="7759b-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="7759b-109">*Cid*</span><span class="sxs-lookup"><span data-stu-id="7759b-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="7759b-110">Identificador del lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="7759b-110">The identifier of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7759b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7759b-111">Return value</span></span>

<span data-ttu-id="7759b-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="7759b-112">This method can return one of these values.</span></span>



| <span data-ttu-id="7759b-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7759b-113">Return code</span></span>                                                                            | <span data-ttu-id="7759b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="7759b-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="7759b-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="7759b-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="7759b-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="7759b-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="7759b-117"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="7759b-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="7759b-118">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="7759b-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7759b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7759b-119">Requirements</span></span>



| <span data-ttu-id="7759b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7759b-120">Requirement</span></span> | <span data-ttu-id="7759b-121">Value</span><span class="sxs-lookup"><span data-stu-id="7759b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7759b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7759b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7759b-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7759b-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7759b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7759b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7759b-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7759b-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7759b-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7759b-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="7759b-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7759b-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7759b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="7759b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7759b-129">**Interfaz ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="7759b-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




