---
description: Expone métodos que permiten que una extensión de Shell proporcione un espacio de nombres de búsqueda.
title: Interfaz IShellFolderSearchable
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 359def5c-d7ad-46bd-bdda-30a7b3eea56c
ms.openlocfilehash: 1f42b3af012361bfd24c93e03c38e6954eb5326e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984631"
---
# <a name="ishellfoldersearchable-interface"></a><span data-ttu-id="fae57-103">Interfaz IShellFolderSearchable</span><span class="sxs-lookup"><span data-stu-id="fae57-103">IShellFolderSearchable interface</span></span>

<span data-ttu-id="fae57-104">Expone métodos que permiten que una extensión de Shell proporcione un espacio de nombres de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="fae57-104">Exposes methods that allow a Shell extension to provide a searchable namespace.</span></span>

## <a name="members"></a><span data-ttu-id="fae57-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="fae57-105">Members</span></span>

<span data-ttu-id="fae57-106">La interfaz **IShellFolderSearchable** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fae57-106">The **IShellFolderSearchable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fae57-107">**IShellFolderSearchable** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fae57-107">**IShellFolderSearchable** also has these types of members:</span></span>

-   [<span data-ttu-id="fae57-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="fae57-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fae57-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="fae57-109">Methods</span></span>

<span data-ttu-id="fae57-110">La interfaz **IShellFolderSearchable** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fae57-110">The **IShellFolderSearchable** interface has these methods.</span></span>



| <span data-ttu-id="fae57-111">Método</span><span class="sxs-lookup"><span data-stu-id="fae57-111">Method</span></span>                                                                | <span data-ttu-id="fae57-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="fae57-112">Description</span></span>                                                               |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="fae57-113">**CancelAsyncSearch**</span><span class="sxs-lookup"><span data-stu-id="fae57-113">**CancelAsyncSearch**</span></span>](ishellfoldersearchable-cancelasyncsearch.md) | <span data-ttu-id="fae57-114">Comienza el proceso de cancelación de una búsqueda asincrónica pendiente.</span><span class="sxs-lookup"><span data-stu-id="fae57-114">Begins the process of canceling a pending asynchronous search.</span></span><br/> |
| [<span data-ttu-id="fae57-115">**FindString**</span><span class="sxs-lookup"><span data-stu-id="fae57-115">**FindString**</span></span>](ishellfoldersearchable-findstring.md)               | <span data-ttu-id="fae57-116">Inicia una búsqueda de una cadena de búsqueda especificada.</span><span class="sxs-lookup"><span data-stu-id="fae57-116">Begins a search for a specified search string.</span></span><br/>                 |
| [<span data-ttu-id="fae57-117">**InvalidateSearch**</span><span class="sxs-lookup"><span data-stu-id="fae57-117">**InvalidateSearch**</span></span>](ishellfoldersearchable-invalidatesearch.md)   | <span data-ttu-id="fae57-118">Convierte este PIDL en una parte no válida de la carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="fae57-118">Makes this PIDL an invalid portion of the Shell folder.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="fae57-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fae57-119">Remarks</span></span>

<span data-ttu-id="fae57-120">Esta interfaz no está definida en ningún archivo de encabezado público.</span><span class="sxs-lookup"><span data-stu-id="fae57-120">This interface is not defined in any public header files.</span></span> <span data-ttu-id="fae57-121">Si decide implementar esta interfaz, puede usar el siguiente código de C/C++ para declarar sus métodos.</span><span class="sxs-lookup"><span data-stu-id="fae57-121">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchable
DECLARE_INTERFACE_IID_(IShellFolderSearchable, IUnknown, "4E1AE66C-204B-11d2-8DB3-0000F87A556C")
{
    // **_ IUnknown methods _*_
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void _*ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // **_ IShellFolderSearchable methods _*_

    // FindString -
    //  The returned Shell folder's enumerator will have any
    //   search hits for the given search string.
    //  punkOnAsyncSearch will be QI'd for IShellFolderSearchableCallback
    STDMETHOD(FindString)(THIS_ LPCWSTR pwszTarget, __inout_opt DWORD _pdwFlags,
                          __in_opt IUnknown *punkOnAsyncSearch, __out LPITEMIDLIST *ppidlOut)   PURE;
    // CancelAsyncSearch -
    //   Begins the process of canceling any pending
    //    asynchronous search from this pidl.
    //    When the search is actually canceled, RunEnd will be called
    //   Returns: S_OK => cancelling, S_FALSE => not running
    STDMETHOD(CancelAsyncSearch) (THIS_ LPCITEMIDLIST pidlSearch, __inout_opt DWORD *pdwFlags) PURE;

    // InvalidateSearch -
    //   Makes this pidl no longer a valid portion of the Shell folder
    //    Also does some cleanup of any databases used in the search and
    //    will cause the eventual release of the callback
    //   May cause async search to be canceled
    STDMETHOD(InvalidateSearch)  (THIS_ LPCITEMIDLIST pidlSearch, __inout_opt DWORD *pdwFlags) PURE;
};
```



## <a name="requirements"></a><span data-ttu-id="fae57-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fae57-122">Requirements</span></span>



| <span data-ttu-id="fae57-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fae57-123">Requirement</span></span> | <span data-ttu-id="fae57-124">Value</span><span class="sxs-lookup"><span data-stu-id="fae57-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fae57-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fae57-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fae57-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fae57-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fae57-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fae57-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fae57-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fae57-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fae57-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fae57-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fae57-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fae57-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
