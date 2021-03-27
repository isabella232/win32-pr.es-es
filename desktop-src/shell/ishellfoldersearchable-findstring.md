---
description: Inicia una búsqueda de una cadena de búsqueda especificada.
ms.assetid: 6ecad03c-e8e0-45ba-8def-b55a029992f2
title: 'IShellFolderSearchable:: FindString (método) (MMC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.FindString
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3e256329bc235f7fe5a0428ba33710fa6b838f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810946"
---
# <a name="ishellfoldersearchablefindstring-method"></a><span data-ttu-id="c4522-103">IShellFolderSearchable:: FindString (método)</span><span class="sxs-lookup"><span data-stu-id="c4522-103">IShellFolderSearchable::FindString method</span></span>

<span data-ttu-id="c4522-104">Inicia una búsqueda de una cadena de búsqueda especificada.</span><span class="sxs-lookup"><span data-stu-id="c4522-104">Begins a search for a specified search string.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4522-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4522-105">Syntax</span></span>


```C++
HRESULT FindString(
  [in]  LPCWSTR      pwszTarget,
  [in]  DWORD        *pdwFlags,
  [in]  IUnknown     *punkOnAsyncSearch,
  [out] LPITEMIDLIST ppidlOut
);
```



## <a name="parameters"></a><span data-ttu-id="c4522-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4522-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4522-107">*pwszTarget* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c4522-107">*pwszTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4522-108">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="c4522-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="c4522-109">Puntero a una cadena que especifica la palabra clave de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c4522-109">A pointer to a string that specifies the search keyword.</span></span>

</dd> <dt>

<span data-ttu-id="c4522-110">*pdwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c4522-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4522-111">Tipo: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="c4522-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="c4522-112">Actualmente no hay marcas definidas; establézcalo en _ \* NULL \* \*.</span><span class="sxs-lookup"><span data-stu-id="c4522-112">No flags are currently defined; set to _\*NULL\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="c4522-113">*punkOnAsyncSearch* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c4522-113">*punkOnAsyncSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4522-114">Tipo: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="c4522-114">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="c4522-115">Un puntero a un objeto de tipo [_ *IUnknown* \*](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="c4522-115">A pointer to an object of type [_ *IUnknown*\*](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="c4522-116">Este objeto debe admitir la interfaz [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) .</span><span class="sxs-lookup"><span data-stu-id="c4522-116">This object must support the [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) interface.</span></span> <span data-ttu-id="c4522-117">Se establece en **null** si no se necesita ninguna devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="c4522-117">Set to **NULL** if no callback is necessary.</span></span>

</dd> <dt>

<span data-ttu-id="c4522-118">*ppidlOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c4522-118">*ppidlOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4522-119">Tipo: **LPITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="c4522-119">Type: **LPITEMIDLIST**</span></span>

<span data-ttu-id="c4522-120">Puntero a una estructura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) para la carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c4522-120">A pointer to an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure for the search folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4522-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4522-121">Return value</span></span>

<span data-ttu-id="c4522-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c4522-122">Type: **HRESULT**</span></span>

<span data-ttu-id="c4522-123">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c4522-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c4522-124">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c4522-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4522-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4522-125">Requirements</span></span>



| <span data-ttu-id="c4522-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4522-126">Requirement</span></span> | <span data-ttu-id="c4522-127">Value</span><span class="sxs-lookup"><span data-stu-id="c4522-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4522-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4522-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c4522-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c4522-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c4522-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4522-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c4522-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c4522-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c4522-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4522-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4522-133"><dt>MMC. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4522-133"><dt>Mmc.h</dt></span></span> </dl>       |
| <span data-ttu-id="c4522-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c4522-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4522-135"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4522-135"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
