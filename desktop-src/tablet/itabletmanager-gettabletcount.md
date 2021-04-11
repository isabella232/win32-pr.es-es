---
description: Recupera el número de tabletas conectadas al sistema.
ms.assetid: b2027336-611b-4d17-8943-f16770effaf8
title: 'ITabletManager:: GetTabletCount (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager.GetTabletCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fbdd485c44bc67b3ecaec5aa279d4bc20e18d167
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279172"
---
# <a name="itabletmanagergettabletcount-method"></a><span data-ttu-id="83113-103">ITabletManager:: GetTabletCount (método)</span><span class="sxs-lookup"><span data-stu-id="83113-103">ITabletManager::GetTabletCount method</span></span>

<span data-ttu-id="83113-104">Recupera el número de tabletas conectadas al sistema.</span><span class="sxs-lookup"><span data-stu-id="83113-104">Retrieves the number of tablets attached to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="83113-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83113-105">Syntax</span></span>


```C++
HRESULT GetTabletCount(
  [out] ULONG *pcTablets
);
```



## <a name="parameters"></a><span data-ttu-id="83113-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83113-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83113-107">*pcTablets* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="83113-107">*pcTablets* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83113-108">El número de tabletas conectadas al sistema.</span><span class="sxs-lookup"><span data-stu-id="83113-108">The number of tablets attached to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83113-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83113-109">Return value</span></span>

<span data-ttu-id="83113-110">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="83113-110">This method can return one of these values.</span></span>



| <span data-ttu-id="83113-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="83113-111">Return code</span></span>                                                                            | <span data-ttu-id="83113-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="83113-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="83113-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="83113-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="83113-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="83113-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="83113-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="83113-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="83113-116">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="83113-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="83113-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83113-117">Requirements</span></span>



| <span data-ttu-id="83113-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="83113-118">Requirement</span></span> | <span data-ttu-id="83113-119">Value</span><span class="sxs-lookup"><span data-stu-id="83113-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83113-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83113-120">Minimum supported client</span></span><br/> | <span data-ttu-id="83113-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="83113-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="83113-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83113-122">Minimum supported server</span></span><br/> | <span data-ttu-id="83113-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="83113-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="83113-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="83113-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="83113-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="83113-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83113-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="83113-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83113-127">**Interfaz ITabletManager**</span><span class="sxs-lookup"><span data-stu-id="83113-127">**ITabletManager Interface**</span></span>](itabletmanager.md)
</dt> </dl>

 

 




