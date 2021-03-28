---
description: Comienza el proceso de cancelación de una búsqueda asincrónica pendiente.
title: 'IShellFolderSearchable:: CancelAsyncSearch (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.CancelAsyncSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5c920dca-fbca-48e1-9dce-38713cf1fcef
ms.openlocfilehash: e9e3231e8cc602a4e00b6ee79a25392717b6e68b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984638"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a><span data-ttu-id="e1b8d-103">IShellFolderSearchable:: CancelAsyncSearch (método)</span><span class="sxs-lookup"><span data-stu-id="e1b8d-103">IShellFolderSearchable::CancelAsyncSearch method</span></span>

<span data-ttu-id="e1b8d-104">Comienza el proceso de cancelación de una búsqueda asincrónica pendiente.</span><span class="sxs-lookup"><span data-stu-id="e1b8d-104">Begins the process of canceling a pending asynchronous search.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1b8d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1b8d-105">Syntax</span></span>


```C++
HRESULT CancelAsyncSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e1b8d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1b8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1b8d-107">*pidlSearch* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e1b8d-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b8d-108">Tipo: **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="e1b8d-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="e1b8d-109">Un puntero a un [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) para la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e1b8d-109">A pointer to an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) for the search.</span></span>

</dd> <dt>

<span data-ttu-id="e1b8d-110">*pdwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e1b8d-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b8d-111">Tipo: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="e1b8d-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="e1b8d-112">Actualmente no hay marcas definidas; establézcalo en _ \* NULL \* \*.</span><span class="sxs-lookup"><span data-stu-id="e1b8d-112">No flags are currently defined; set to _\*NULL\*\*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1b8d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1b8d-113">Return value</span></span>

<span data-ttu-id="e1b8d-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e1b8d-114">Type: **HRESULT**</span></span>

<span data-ttu-id="e1b8d-115">Devuelve S \_ OK si se cancela o s \_ false si la búsqueda no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="e1b8d-115">Returns S\_OK if canceling, or S\_FALSE if search is not running.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1b8d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1b8d-116">Remarks</span></span>

<span data-ttu-id="e1b8d-117">Cuando la búsqueda se cancela realmente, se llamará a [**RunEnd**](ishellfoldersearchablecallback-runend.md) .</span><span class="sxs-lookup"><span data-stu-id="e1b8d-117">When the search is actually canceled, [**RunEnd**](ishellfoldersearchablecallback-runend.md) will be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1b8d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1b8d-118">Requirements</span></span>



| <span data-ttu-id="e1b8d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1b8d-119">Requirement</span></span> | <span data-ttu-id="e1b8d-120">Value</span><span class="sxs-lookup"><span data-stu-id="e1b8d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b8d-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1b8d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e1b8d-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e1b8d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e1b8d-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1b8d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e1b8d-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e1b8d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e1b8d-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e1b8d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1b8d-126"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1b8d-126"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




