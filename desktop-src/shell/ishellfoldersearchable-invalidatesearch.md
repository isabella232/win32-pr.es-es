---
description: Convierte este puntero a una lista de identificadores de elemento (PIDL) en una parte no válida de la carpeta de Shell.
title: 'IShellFolderSearchable:: InvalidateSearch (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.InvalidateSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6985a299-8547-4db4-99f9-d46dafe4789b
ms.openlocfilehash: 36c1de0a606fdfddbe8eb74b5cc6c20cdda8e983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275676"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a><span data-ttu-id="fcdbb-103">IShellFolderSearchable:: InvalidateSearch (método)</span><span class="sxs-lookup"><span data-stu-id="fcdbb-103">IShellFolderSearchable::InvalidateSearch method</span></span>

<span data-ttu-id="fcdbb-104">Convierte este puntero a una lista de identificadores de elemento (PIDL) en una parte no válida de la carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="fcdbb-104">Makes this pointer to an item identifier list (PIDL) an invalid portion of the Shell folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcdbb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fcdbb-105">Syntax</span></span>


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="fcdbb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fcdbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcdbb-107">*pidlSearch* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fcdbb-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcdbb-108">Tipo: **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="fcdbb-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="fcdbb-109">Un puntero a la estructura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) para la carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="fcdbb-109">A pointer to the [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure for the search folder.</span></span>

</dd> <dt>

<span data-ttu-id="fcdbb-110">*pdwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fcdbb-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcdbb-111">Tipo: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="fcdbb-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="fcdbb-112">Actualmente no hay marcas definidas; establézcalo en _ \* NULL \* \*.</span><span class="sxs-lookup"><span data-stu-id="fcdbb-112">No flags are currently defined; set to _\*NULL\*\*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcdbb-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fcdbb-113">Return value</span></span>

<span data-ttu-id="fcdbb-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fcdbb-114">Type: **HRESULT**</span></span>

<span data-ttu-id="fcdbb-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="fcdbb-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fcdbb-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fcdbb-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcdbb-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fcdbb-117">Remarks</span></span>

<span data-ttu-id="fcdbb-118">Cuando se invalida una carpeta de búsqueda, puede realizar la limpieza de los recursos que ha usado.</span><span class="sxs-lookup"><span data-stu-id="fcdbb-118">When a search folder is invalidated, it can perform cleanup of any resources it has used.</span></span> <span data-ttu-id="fcdbb-119">El método **IShellFolderSearchable:: InvalidateSearch** puede hacer que se cancele una búsqueda asincrónica y dará como resultado la versión final del objeto de interfaz [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) .</span><span class="sxs-lookup"><span data-stu-id="fcdbb-119">The **IShellFolderSearchable::InvalidateSearch** method may cause an asynchronous search to be canceled and will result in the eventual release of the [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) interface object.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcdbb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcdbb-120">Requirements</span></span>



| <span data-ttu-id="fcdbb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcdbb-121">Requirement</span></span> | <span data-ttu-id="fcdbb-122">Value</span><span class="sxs-lookup"><span data-stu-id="fcdbb-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcdbb-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fcdbb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fcdbb-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fcdbb-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fcdbb-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fcdbb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fcdbb-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fcdbb-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fcdbb-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fcdbb-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcdbb-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcdbb-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




