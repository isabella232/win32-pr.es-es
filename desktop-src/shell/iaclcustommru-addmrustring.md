---
description: Agrega una entrada a la lista de mru usada más recientemente.
title: IACLCustomMRU::AddMRUString (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.AddMRUString
api_type:
- COM
api_location: ''
ms.assetid: d8fb8fa5-452b-45fd-b015-d9bf3d0c642e
ms.openlocfilehash: 300474dde82274c668e52d9fe9910634d0ac904c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842006"
---
# <a name="iaclcustommruaddmrustring-method"></a><span data-ttu-id="9c8b3-103">IACLCustomMRU::AddMRUString (método)</span><span class="sxs-lookup"><span data-stu-id="9c8b3-103">IACLCustomMRU::AddMRUString method</span></span>

<span data-ttu-id="9c8b3-104">Agrega una entrada a la lista de MRU usada más recientemente.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-104">Adds an entry to the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c8b3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c8b3-105">Syntax</span></span>


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a><span data-ttu-id="9c8b3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c8b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c8b3-107">*pwszEntry* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9c8b3-107">*pwszEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c8b3-108">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="9c8b3-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="9c8b3-109">Puntero a un búfer que contiene la nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-109">A pointer to a buffer containing the new entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c8b3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c8b3-110">Return value</span></span>

<span data-ttu-id="9c8b3-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9c8b3-111">Type: **HRESULT**</span></span>

<span data-ttu-id="9c8b3-112">Si este método se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9c8b3-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9c8b3-113">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="9c8b3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c8b3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c8b3-114">Requirements</span></span>



| <span data-ttu-id="9c8b3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c8b3-115">Requirement</span></span> | <span data-ttu-id="9c8b3-116">Value</span><span class="sxs-lookup"><span data-stu-id="9c8b3-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9c8b3-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c8b3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9c8b3-118">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="9c8b3-118">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="9c8b3-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c8b3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9c8b3-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c8b3-120">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




