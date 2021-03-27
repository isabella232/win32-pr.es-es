---
description: Expone rutinas de devolución de llamada para supervisar el proceso de búsqueda.
title: Interfaz IShellFolderSearchableCallback
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
ms.openlocfilehash: aac648861f3bf9dc5ae8fdcc7173792e427b234f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997277"
---
# <a name="ishellfoldersearchablecallback-interface"></a><span data-ttu-id="9c2be-103">Interfaz IShellFolderSearchableCallback</span><span class="sxs-lookup"><span data-stu-id="9c2be-103">IShellFolderSearchableCallback interface</span></span>

<span data-ttu-id="9c2be-104">Expone rutinas de devolución de llamada para supervisar el proceso de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9c2be-104">Exposes callback routines to monitor the search process.</span></span>

## <a name="members"></a><span data-ttu-id="9c2be-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="9c2be-105">Members</span></span>

<span data-ttu-id="9c2be-106">La interfaz **IShellFolderSearchableCallback** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9c2be-106">The **IShellFolderSearchableCallback** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9c2be-107">**IShellFolderSearchableCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9c2be-107">**IShellFolderSearchableCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="9c2be-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="9c2be-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9c2be-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="9c2be-109">Methods</span></span>

<span data-ttu-id="9c2be-110">La interfaz **IShellFolderSearchableCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9c2be-110">The **IShellFolderSearchableCallback** interface has these methods.</span></span>



| <span data-ttu-id="9c2be-111">Método</span><span class="sxs-lookup"><span data-stu-id="9c2be-111">Method</span></span>                                                      | <span data-ttu-id="9c2be-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c2be-112">Description</span></span>                                      |
|:------------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="9c2be-113">**RunBegin**</span><span class="sxs-lookup"><span data-stu-id="9c2be-113">**RunBegin**</span></span>](ishellfoldersearchablecallback-runbegin.md) | <span data-ttu-id="9c2be-114">Indica que se ha iniciado una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9c2be-114">Indicates that a search was started.</span></span><br/>  |
| [<span data-ttu-id="9c2be-115">**RunEnd**</span><span class="sxs-lookup"><span data-stu-id="9c2be-115">**RunEnd**</span></span>](ishellfoldersearchablecallback-runend.md)     | <span data-ttu-id="9c2be-116">Indica que ha finalizado una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9c2be-116">Indicates that a search has finished.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9c2be-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c2be-117">Remarks</span></span>

<span data-ttu-id="9c2be-118">Esta interfaz no está definida en ningún archivo de encabezado público.</span><span class="sxs-lookup"><span data-stu-id="9c2be-118">This interface is not defined in any public header files.</span></span> <span data-ttu-id="9c2be-119">Si decide implementar esta interfaz, puede usar el siguiente código de C/C++ para declarar sus métodos.</span><span class="sxs-lookup"><span data-stu-id="9c2be-119">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchableCallback
DECLARE_INTERFACE_IID_(IShellFolderSearchableCallback, IUnknown, "F98D8294-2BBC-11d2-8DBD-0000F87A556C")
{
    // **_ IUnknown methods _*_
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void _*ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // **_ IShellFolderSearchableCallback Methods _**

    STDMETHOD(RunBegin)(THIS_ DWORD dwReserved) PURE;
    STDMETHOD(RunEnd)(THIS_ DWORD dwReserved) PURE;
};
```



## <a name="requirements"></a><span data-ttu-id="9c2be-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c2be-120">Requirements</span></span>



| <span data-ttu-id="9c2be-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c2be-121">Requirement</span></span> | <span data-ttu-id="9c2be-122">Value</span><span class="sxs-lookup"><span data-stu-id="9c2be-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c2be-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c2be-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9c2be-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9c2be-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9c2be-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c2be-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9c2be-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9c2be-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9c2be-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9c2be-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c2be-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c2be-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
