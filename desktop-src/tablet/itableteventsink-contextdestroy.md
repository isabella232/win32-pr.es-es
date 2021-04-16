---
description: Se produce cuando se destruye un contexto de Tablet PC.
ms.assetid: 805289d8-267e-488b-8092-6b07b37dd6d4
title: 'ITabletEventSink:: ContextDestroy (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.ContextDestroy
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c9b5d78d4ce4032c1a7a2082fb749afc5a39949a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546734"
---
# <a name="itableteventsinkcontextdestroy-method"></a><span data-ttu-id="60d10-103">ITabletEventSink:: ContextDestroy (método)</span><span class="sxs-lookup"><span data-stu-id="60d10-103">ITabletEventSink::ContextDestroy method</span></span>

<span data-ttu-id="60d10-104">Se produce cuando se destruye un contexto de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="60d10-104">Occurs when a tablet context is being destroyed.</span></span>

## <a name="syntax"></a><span data-ttu-id="60d10-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60d10-105">Syntax</span></span>


```C++
HRESULT ContextDestroy(
  [in] TABLET_CONTEXT_ID tcid
);
```



## <a name="parameters"></a><span data-ttu-id="60d10-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60d10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60d10-107">*TCID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="60d10-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60d10-108">Identificador del contexto de Tablet PC que se va a destruir.</span><span class="sxs-lookup"><span data-stu-id="60d10-108">The identifier of the tablet context being destroyed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60d10-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60d10-109">Return value</span></span>

<span data-ttu-id="60d10-110">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="60d10-110">This method can return one of these values.</span></span>



| <span data-ttu-id="60d10-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="60d10-111">Return code</span></span>                                                                            | <span data-ttu-id="60d10-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="60d10-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="60d10-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="60d10-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="60d10-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="60d10-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="60d10-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="60d10-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="60d10-116">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="60d10-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="60d10-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60d10-117">Requirements</span></span>



| <span data-ttu-id="60d10-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="60d10-118">Requirement</span></span> | <span data-ttu-id="60d10-119">Value</span><span class="sxs-lookup"><span data-stu-id="60d10-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="60d10-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60d10-120">Minimum supported client</span></span><br/> | <span data-ttu-id="60d10-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="60d10-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="60d10-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60d10-122">Minimum supported server</span></span><br/> | <span data-ttu-id="60d10-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="60d10-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="60d10-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="60d10-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="60d10-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="60d10-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60d10-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="60d10-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60d10-127">**Interfaz ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="60d10-127">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




