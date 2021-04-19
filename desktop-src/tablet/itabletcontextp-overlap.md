---
description: Mueve un contexto de tableta al principio o al final de la cola de entrada.
ms.assetid: ef4521b5-776b-46dc-864a-625bc221054a
title: 'ITabletContextP:: superposición (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.Overlap
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: b009bc08dddb15bc7aa5b12c8846ea66c4a52e56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716718"
---
# <a name="itabletcontextpoverlap-method"></a><span data-ttu-id="0cb56-103">ITabletContextP:: superposición (método)</span><span class="sxs-lookup"><span data-stu-id="0cb56-103">ITabletContextP::Overlap method</span></span>

<span data-ttu-id="0cb56-104">Mueve un contexto de tableta al principio o al final de la cola de entrada.</span><span class="sxs-lookup"><span data-stu-id="0cb56-104">Moves a tablet context to the front or back of the input queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb56-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0cb56-105">Syntax</span></span>


```C++
HRESULT Overlap(
  [in]  BOOL  bTop,
  [out] DWORD *pdwtcid
);
```



## <a name="parameters"></a><span data-ttu-id="0cb56-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0cb56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cb56-107">*bTop* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0cb56-107">*bTop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb56-108">Indica si el contexto de Tablet PC debe moverse a la parte superior o inferior de la cola de entrada.</span><span class="sxs-lookup"><span data-stu-id="0cb56-108">Indicates if the tablet context should be moved to the top or bottom of the input queue.</span></span>

</dd> <dt>

<span data-ttu-id="0cb56-109">*pdwtcid* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0cb56-109">*pdwtcid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb56-110">Identificador de contexto de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="0cb56-110">The tablet context identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cb56-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0cb56-111">Return value</span></span>

<span data-ttu-id="0cb56-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0cb56-112">This method can return one of these values.</span></span>



| <span data-ttu-id="0cb56-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0cb56-113">Return code</span></span>                                                                            | <span data-ttu-id="0cb56-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="0cb56-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="0cb56-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0cb56-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="0cb56-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="0cb56-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="0cb56-117"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="0cb56-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="0cb56-118">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="0cb56-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0cb56-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cb56-119">Requirements</span></span>



| <span data-ttu-id="0cb56-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cb56-120">Requirement</span></span> | <span data-ttu-id="0cb56-121">Value</span><span class="sxs-lookup"><span data-stu-id="0cb56-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb56-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cb56-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0cb56-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0cb56-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0cb56-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cb56-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0cb56-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0cb56-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0cb56-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0cb56-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="0cb56-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0cb56-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cb56-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cb56-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb56-129">**Interfaz ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="0cb56-129">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




