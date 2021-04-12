---
description: Se produce cuando se crea un nuevo contexto de Tablet PC.
ms.assetid: 64e1f778-90c1-417d-a80b-37aeecffd411
title: 'ITabletEventSink:: ContextCreate (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.ContextCreate
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: e622a246c7c317cf9e3373cbd3791108ed071e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361481"
---
# <a name="itableteventsinkcontextcreate-method"></a><span data-ttu-id="3ad24-103">ITabletEventSink:: ContextCreate (método)</span><span class="sxs-lookup"><span data-stu-id="3ad24-103">ITabletEventSink::ContextCreate method</span></span>

<span data-ttu-id="3ad24-104">Se produce cuando se crea un nuevo contexto de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="3ad24-104">Occurs when a new tablet context is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ad24-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ad24-105">Syntax</span></span>


```C++
HRESULT ContextCreate(
  [in] TABLET_CONTEXT_ID tcid
);
```



## <a name="parameters"></a><span data-ttu-id="3ad24-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3ad24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ad24-107">*TCID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3ad24-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ad24-108">Identificador del contexto de Tablet PC que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="3ad24-108">The identifier of the tablet context being created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ad24-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3ad24-109">Return value</span></span>

<span data-ttu-id="3ad24-110">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="3ad24-110">This method can return one of these values.</span></span>



| <span data-ttu-id="3ad24-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3ad24-111">Return code</span></span>                                                                            | <span data-ttu-id="3ad24-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ad24-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="3ad24-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3ad24-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="3ad24-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="3ad24-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="3ad24-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="3ad24-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="3ad24-116">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="3ad24-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3ad24-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ad24-117">Requirements</span></span>



| <span data-ttu-id="3ad24-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ad24-118">Requirement</span></span> | <span data-ttu-id="3ad24-119">Value</span><span class="sxs-lookup"><span data-stu-id="3ad24-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ad24-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ad24-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3ad24-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3ad24-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3ad24-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ad24-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3ad24-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3ad24-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3ad24-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ad24-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ad24-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ad24-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ad24-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ad24-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ad24-127">**Interfaz ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="3ad24-127">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




