---
description: Expone rutinas de devolución de llamada para supervisar el proceso de búsqueda.
title: IShellFolderSearchableCallback (interfaz)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3412a01b-d5ea-44e1-819c-f10f81fac391
ms.openlocfilehash: cf1a3b03eed2a15e82e1313875a4ab8584243190
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842786"
---
# <a name="ishellfoldersearchablecallback-interface"></a><span data-ttu-id="545d8-103">IShellFolderSearchableCallback (interfaz)</span><span class="sxs-lookup"><span data-stu-id="545d8-103">IShellFolderSearchableCallback interface</span></span>

<span data-ttu-id="545d8-104">Expone rutinas de devolución de llamada para supervisar el proceso de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="545d8-104">Exposes callback routines to monitor the search process.</span></span>

## <a name="members"></a><span data-ttu-id="545d8-105">Members</span><span class="sxs-lookup"><span data-stu-id="545d8-105">Members</span></span>

<span data-ttu-id="545d8-106">La **interfaz IShellFolderSearchableCallback** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="545d8-106">The **IShellFolderSearchableCallback** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="545d8-107">**IShellFolderSearchableCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="545d8-107">**IShellFolderSearchableCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="545d8-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="545d8-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="545d8-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="545d8-109">Methods</span></span>

<span data-ttu-id="545d8-110">La **interfaz IShellFolderSearchableCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="545d8-110">The **IShellFolderSearchableCallback** interface has these methods.</span></span>



| <span data-ttu-id="545d8-111">Método</span><span class="sxs-lookup"><span data-stu-id="545d8-111">Method</span></span>                                                      | <span data-ttu-id="545d8-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="545d8-112">Description</span></span>                                      |
|:------------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="545d8-113">**RunBegin**</span><span class="sxs-lookup"><span data-stu-id="545d8-113">**RunBegin**</span></span>](ishellfoldersearchablecallback-runbegin.md) | <span data-ttu-id="545d8-114">Indica que se inició una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="545d8-114">Indicates that a search was started.</span></span><br/>  |
| [<span data-ttu-id="545d8-115">**RunEnd**</span><span class="sxs-lookup"><span data-stu-id="545d8-115">**RunEnd**</span></span>](ishellfoldersearchablecallback-runend.md)     | <span data-ttu-id="545d8-116">Indica que ha finalizado una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="545d8-116">Indicates that a search has finished.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="545d8-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="545d8-117">Remarks</span></span>

<span data-ttu-id="545d8-118">Esta interfaz no se define en ningún archivo de encabezado público.</span><span class="sxs-lookup"><span data-stu-id="545d8-118">This interface is not defined in any public header files.</span></span> <span data-ttu-id="545d8-119">Si decide implementar esta interfaz, puede usar el siguiente código de C/C++ para declarar sus métodos.</span><span class="sxs-lookup"><span data-stu-id="545d8-119">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchableCallback
DECLARE_INTERFACE_IID_(IShellFolderSearchableCallback, IUnknown, "F98D8294-2BBC-11d2-8DBD-0000F87A556C")
{
    // *** IUnknown methods ***
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void **ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // *** IShellFolderSearchableCallback Methods ***

    STDMETHOD(RunBegin)(THIS_ DWORD dwReserved) PURE;
    STDMETHOD(RunEnd)(THIS_ DWORD dwReserved) PURE;
};
```



## <a name="requirements"></a><span data-ttu-id="545d8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="545d8-120">Requirements</span></span>



| <span data-ttu-id="545d8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="545d8-121">Requirement</span></span> | <span data-ttu-id="545d8-122">Value</span><span class="sxs-lookup"><span data-stu-id="545d8-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="545d8-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="545d8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="545d8-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="545d8-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="545d8-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="545d8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="545d8-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="545d8-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="545d8-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="545d8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="545d8-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="545d8-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
