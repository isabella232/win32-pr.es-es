---
description: Agrega una entrada a la lista de elementos usados más recientemente (MRU).
title: 'IACLCustomMRU:: AddMRUString (método)'
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
ms.openlocfilehash: d2f444041f466b367f3d4532f65029bcc69c3683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997685"
---
# <a name="iaclcustommruaddmrustring-method"></a><span data-ttu-id="1afb8-103">IACLCustomMRU:: AddMRUString (método)</span><span class="sxs-lookup"><span data-stu-id="1afb8-103">IACLCustomMRU::AddMRUString method</span></span>

<span data-ttu-id="1afb8-104">Agrega una entrada a la lista de elementos usados más recientemente (MRU).</span><span class="sxs-lookup"><span data-stu-id="1afb8-104">Adds an entry to the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="1afb8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1afb8-105">Syntax</span></span>


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a><span data-ttu-id="1afb8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1afb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1afb8-107">*pwszEntry* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1afb8-107">*pwszEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1afb8-108">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="1afb8-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="1afb8-109">Puntero a un búfer que contiene la nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="1afb8-109">A pointer to a buffer containing the new entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1afb8-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1afb8-110">Return value</span></span>

<span data-ttu-id="1afb8-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1afb8-111">Type: **HRESULT**</span></span>

<span data-ttu-id="1afb8-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1afb8-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1afb8-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1afb8-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1afb8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1afb8-114">Requirements</span></span>



| <span data-ttu-id="1afb8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1afb8-115">Requirement</span></span> | <span data-ttu-id="1afb8-116">Value</span><span class="sxs-lookup"><span data-stu-id="1afb8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1afb8-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1afb8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1afb8-118">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="1afb8-118">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="1afb8-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1afb8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1afb8-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1afb8-120">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




