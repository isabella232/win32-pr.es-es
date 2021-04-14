---
description: Recupera el identificador del lápiz óptico.
ms.assetid: 27320a2f-1e4a-4d7d-a1f8-5244f4a03415
title: 'ITabletCursor:: GetId (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5d4f71d2cd465bfd2d1ff4c245154a300c431df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423987"
---
# <a name="itabletcursorgetid-method"></a><span data-ttu-id="d8154-103">ITabletCursor:: GetId (método)</span><span class="sxs-lookup"><span data-stu-id="d8154-103">ITabletCursor::GetId method</span></span>

<span data-ttu-id="d8154-104">Recupera el identificador del lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="d8154-104">Retrieves the stylus identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8154-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8154-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] CURSOR_ID *pCid
);
```



## <a name="parameters"></a><span data-ttu-id="d8154-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8154-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8154-107">*pCid* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d8154-107">*pCid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8154-108">Identificador del lápiz de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="d8154-108">The identifier of the tablet stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8154-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8154-109">Return value</span></span>

<span data-ttu-id="d8154-110">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="d8154-110">This method can return one of these values.</span></span>



| <span data-ttu-id="d8154-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d8154-111">Return code</span></span>                                                                            | <span data-ttu-id="d8154-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8154-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="d8154-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d8154-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="d8154-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="d8154-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="d8154-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="d8154-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="d8154-116">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="d8154-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d8154-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8154-117">Remarks</span></span>

<span data-ttu-id="d8154-118">\_El ID. de cursor se define como un valor DWORD.</span><span class="sxs-lookup"><span data-stu-id="d8154-118">CURSOR\_ID is defined as a DWORD.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8154-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8154-119">Requirements</span></span>



| <span data-ttu-id="d8154-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8154-120">Requirement</span></span> | <span data-ttu-id="d8154-121">Value</span><span class="sxs-lookup"><span data-stu-id="d8154-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8154-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8154-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d8154-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d8154-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d8154-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8154-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d8154-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d8154-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d8154-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8154-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="d8154-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d8154-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8154-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8154-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8154-129">**Interfaz ITabletCursor**</span><span class="sxs-lookup"><span data-stu-id="d8154-129">**ITabletCursor Interface**</span></span>](itabletcursor.md)
</dt> </dl>

 

 




