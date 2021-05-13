---
description: Comienza el proceso de cancelación de una búsqueda asincrónica pendiente.
title: IShellFolderSearchable::CancelAsyncSearch (método)
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
ms.openlocfilehash: 3146fea4f6c8d8547c8c86096b434cbaea5b5926
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842996"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a><span data-ttu-id="d78d0-103">IShellFolderSearchable::CancelAsyncSearch (método)</span><span class="sxs-lookup"><span data-stu-id="d78d0-103">IShellFolderSearchable::CancelAsyncSearch method</span></span>

<span data-ttu-id="d78d0-104">Comienza el proceso de cancelación de una búsqueda asincrónica pendiente.</span><span class="sxs-lookup"><span data-stu-id="d78d0-104">Begins the process of canceling a pending asynchronous search.</span></span>

## <a name="syntax"></a><span data-ttu-id="d78d0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d78d0-105">Syntax</span></span>


```C++
HRESULT CancelAsyncSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d78d0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d78d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d78d0-107">*pidlSearch* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d78d0-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d78d0-108">Tipo: **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="d78d0-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="d78d0-109">Puntero a [**itemidlist para**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d78d0-109">A pointer to an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) for the search.</span></span>

</dd> <dt>

<span data-ttu-id="d78d0-110">*pdwFlags* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d78d0-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d78d0-111">Tipo: **DWORD \***</span><span class="sxs-lookup"><span data-stu-id="d78d0-111">Type: **DWORD\***</span></span>

<span data-ttu-id="d78d0-112">No hay marcas definidas actualmente; se establece en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="d78d0-112">No flags are currently defined; set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d78d0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d78d0-113">Return value</span></span>

<span data-ttu-id="d78d0-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d78d0-114">Type: **HRESULT**</span></span>

<span data-ttu-id="d78d0-115">Devuelve S \_ OK si se cancela, o S FALSE \_ si la búsqueda no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="d78d0-115">Returns S\_OK if canceling, or S\_FALSE if search is not running.</span></span>

## <a name="remarks"></a><span data-ttu-id="d78d0-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d78d0-116">Remarks</span></span>

<span data-ttu-id="d78d0-117">Cuando la búsqueda se cancele realmente, se llamará a [**RunEnd.**](ishellfoldersearchablecallback-runend.md)</span><span class="sxs-lookup"><span data-stu-id="d78d0-117">When the search is actually canceled, [**RunEnd**](ishellfoldersearchablecallback-runend.md) will be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="d78d0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d78d0-118">Requirements</span></span>



| <span data-ttu-id="d78d0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d78d0-119">Requirement</span></span> | <span data-ttu-id="d78d0-120">Value</span><span class="sxs-lookup"><span data-stu-id="d78d0-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d78d0-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d78d0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d78d0-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d78d0-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d78d0-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d78d0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d78d0-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d78d0-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d78d0-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d78d0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d78d0-126"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d78d0-126"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




