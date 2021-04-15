---
description: Se produce cuando un lápiz entra dentro del intervalo de detección del digitalizador.
ms.assetid: 22be233a-fc33-4a8f-91b6-28b2f2910b69
title: 'ITabletEventSink:: CursorInRange (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorInRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: eec2b4f309480ecaecd50de2120d701c916b6fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688606"
---
# <a name="itableteventsinkcursorinrange-method"></a><span data-ttu-id="15911-103">ITabletEventSink:: CursorInRange (método)</span><span class="sxs-lookup"><span data-stu-id="15911-103">ITabletEventSink::CursorInRange method</span></span>

<span data-ttu-id="15911-104">Se produce cuando un lápiz entra dentro del intervalo de detección del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="15911-104">Occurs when a stylus comes within the digitizer's range of detection.</span></span>

## <a name="syntax"></a><span data-ttu-id="15911-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15911-105">Syntax</span></span>


```C++
HRESULT CursorInRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="15911-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15911-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15911-107">*TCID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="15911-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15911-108">Identificador del objeto de tableta que detectó el lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="15911-108">The identifier of the tablet object that detected the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="15911-109">*Cid*</span><span class="sxs-lookup"><span data-stu-id="15911-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="15911-110">Identificador del objeto de lápiz óptico incluido en el intervalo del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="15911-110">The identifier of the stylus object that has come in range of the digitizer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15911-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15911-111">Return value</span></span>

<span data-ttu-id="15911-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="15911-112">This method can return one of these values.</span></span>



| <span data-ttu-id="15911-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="15911-113">Return code</span></span>                                                                            | <span data-ttu-id="15911-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="15911-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="15911-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="15911-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="15911-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="15911-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="15911-117"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="15911-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="15911-118">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="15911-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="15911-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15911-119">Requirements</span></span>



| <span data-ttu-id="15911-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="15911-120">Requirement</span></span> | <span data-ttu-id="15911-121">Value</span><span class="sxs-lookup"><span data-stu-id="15911-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="15911-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15911-122">Minimum supported client</span></span><br/> | <span data-ttu-id="15911-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="15911-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="15911-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15911-124">Minimum supported server</span></span><br/> | <span data-ttu-id="15911-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="15911-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="15911-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15911-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="15911-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15911-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15911-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="15911-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15911-129">**Interfaz ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="15911-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




