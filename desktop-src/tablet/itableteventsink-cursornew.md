---
description: Se produce cuando se agrega un nuevo lápiz al sistema.
ms.assetid: bd0f0d2a-c0d9-48fc-bc90-f63f038639f3
title: 'ITabletEventSink:: CursorNew (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorNew
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 31db152eb15d6f980234dc556e277691d3f14959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279175"
---
# <a name="itableteventsinkcursornew-method"></a><span data-ttu-id="170d7-103">ITabletEventSink:: CursorNew (método)</span><span class="sxs-lookup"><span data-stu-id="170d7-103">ITabletEventSink::CursorNew method</span></span>

<span data-ttu-id="170d7-104">Se produce cuando se agrega un nuevo lápiz al sistema.</span><span class="sxs-lookup"><span data-stu-id="170d7-104">Occurs when a new stylus is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="170d7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="170d7-105">Syntax</span></span>


```C++
HRESULT CursorNew(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="170d7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="170d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="170d7-107">*TCID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="170d7-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="170d7-108">Identificador del contexto de Tablet PC en el que se agregó el nuevo lápiz.</span><span class="sxs-lookup"><span data-stu-id="170d7-108">The identifier of the tablet context where the new stylus was added.</span></span>

</dd> <dt>

<span data-ttu-id="170d7-109">*Cid*</span><span class="sxs-lookup"><span data-stu-id="170d7-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="170d7-110">Identificador del nuevo objeto de lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="170d7-110">The identifier of the new stylus object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="170d7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="170d7-111">Return value</span></span>

<span data-ttu-id="170d7-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="170d7-112">This method can return one of these values.</span></span>



| <span data-ttu-id="170d7-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="170d7-113">Return code</span></span>                                                                            | <span data-ttu-id="170d7-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="170d7-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="170d7-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="170d7-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="170d7-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="170d7-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="170d7-117"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="170d7-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="170d7-118">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="170d7-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="170d7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="170d7-119">Requirements</span></span>



| <span data-ttu-id="170d7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="170d7-120">Requirement</span></span> | <span data-ttu-id="170d7-121">Value</span><span class="sxs-lookup"><span data-stu-id="170d7-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="170d7-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="170d7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="170d7-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="170d7-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="170d7-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="170d7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="170d7-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="170d7-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="170d7-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="170d7-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="170d7-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="170d7-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="170d7-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="170d7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="170d7-129">**Interfaz ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="170d7-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




