---
description: Recupera el objeto de botón especificado de un lápiz de Tablet PC.
ms.assetid: 83a26703-4501-4f43-9e86-c5c753347012
title: 'ITabletCursor:: GetButton (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 0b9e8e1337cacdb26d8c124d10e0a886748e70fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716453"
---
# <a name="itabletcursorgetbutton-method"></a><span data-ttu-id="85b9a-103">ITabletCursor:: GetButton (método)</span><span class="sxs-lookup"><span data-stu-id="85b9a-103">ITabletCursor::GetButton method</span></span>

<span data-ttu-id="85b9a-104">Recupera el objeto de botón especificado de un lápiz de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="85b9a-104">Retrieves the specified button object from a tablet stylus.</span></span>

## <a name="syntax"></a><span data-ttu-id="85b9a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85b9a-105">Syntax</span></span>


```C++
HRESULT GetButton(
  [in]  ULONG               iButton,
  [out] ITabletCursorButton **ppButton
);
```



## <a name="parameters"></a><span data-ttu-id="85b9a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85b9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85b9a-107">*iButton* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85b9a-107">*iButton* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85b9a-108">Identificador del botón que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="85b9a-108">Identifier of the button to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="85b9a-109">*ppButton* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="85b9a-109">*ppButton* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85b9a-110">El objeto de botón especificado por el parámetro *iButton* .</span><span class="sxs-lookup"><span data-stu-id="85b9a-110">The button object specified by the *iButton* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85b9a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85b9a-111">Return value</span></span>

<span data-ttu-id="85b9a-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="85b9a-112">This method can return one of these values.</span></span>



| <span data-ttu-id="85b9a-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="85b9a-113">Return code</span></span>                                                                            | <span data-ttu-id="85b9a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="85b9a-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="85b9a-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="85b9a-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="85b9a-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="85b9a-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="85b9a-117"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="85b9a-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="85b9a-118">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="85b9a-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="85b9a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85b9a-119">Requirements</span></span>



| <span data-ttu-id="85b9a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="85b9a-120">Requirement</span></span> | <span data-ttu-id="85b9a-121">Value</span><span class="sxs-lookup"><span data-stu-id="85b9a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85b9a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85b9a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="85b9a-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="85b9a-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="85b9a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85b9a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="85b9a-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="85b9a-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="85b9a-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="85b9a-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="85b9a-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="85b9a-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85b9a-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="85b9a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85b9a-129">**Interfaz ITabletCursor**</span><span class="sxs-lookup"><span data-stu-id="85b9a-129">**ITabletCursor Interface**</span></span>](itabletcursor.md)
</dt> </dl>

 

 




