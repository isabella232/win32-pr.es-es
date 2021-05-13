---
description: Expone métodos que permiten que una carpeta de Shell admita vistas diferentes en su contenido (diferentes diseños jerárquicos de sus datos).
title: IShellFolderViewType (interfaz)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9b597f6b-ef27-4fa1-ad00-e131dbd979e7
ms.openlocfilehash: f3ccb4073d59e0ebe9b840bd6f8f592f463e1e46
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842696"
---
# <a name="ishellfolderviewtype-interface"></a><span data-ttu-id="40e69-103">IShellFolderViewType (interfaz)</span><span class="sxs-lookup"><span data-stu-id="40e69-103">IShellFolderViewType interface</span></span>

<span data-ttu-id="40e69-104">Expone métodos que permiten que una carpeta de Shell admita vistas diferentes en su contenido (diferentes diseños jerárquicos de sus datos).</span><span class="sxs-lookup"><span data-stu-id="40e69-104">Exposes methods that enable a Shell folder to support different views on its content (different hierarchical layouts of its data).</span></span>

## <a name="members"></a><span data-ttu-id="40e69-105">Members</span><span class="sxs-lookup"><span data-stu-id="40e69-105">Members</span></span>

<span data-ttu-id="40e69-106">La **interfaz IShellFolderViewType** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="40e69-106">The **IShellFolderViewType** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="40e69-107">**IShellFolderViewType** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="40e69-107">**IShellFolderViewType** also has these types of members:</span></span>

-   [<span data-ttu-id="40e69-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="40e69-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="40e69-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="40e69-109">Methods</span></span>

<span data-ttu-id="40e69-110">La **interfaz IShellFolderViewType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="40e69-110">The **IShellFolderViewType** interface has these methods.</span></span>



| <span data-ttu-id="40e69-111">Método</span><span class="sxs-lookup"><span data-stu-id="40e69-111">Method</span></span>                                                                      | <span data-ttu-id="40e69-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="40e69-112">Description</span></span>                                                                                                                                                          |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40e69-113">**EnumViews**</span><span class="sxs-lookup"><span data-stu-id="40e69-113">**EnumViews**</span></span>](ishellfolderviewtype-enumviews.md)                         | <span data-ttu-id="40e69-114">Recupera un enumerador que devolverá un PIDL para cada vista extendida.</span><span class="sxs-lookup"><span data-stu-id="40e69-114">Retrieves an enumerator that will return one PIDL for every extended view.</span></span><br/>                                                                                |
| [<span data-ttu-id="40e69-115">**GetDefaultViewName**</span><span class="sxs-lookup"><span data-stu-id="40e69-115">**GetDefaultViewName**</span></span>](ishellfolderviewtype-getdefaultviewname.md)       | <span data-ttu-id="40e69-116">Obtiene el nombre de la vista predeterminada.</span><span class="sxs-lookup"><span data-stu-id="40e69-116">Gets the name of the default view.</span></span> <span data-ttu-id="40e69-117">Llame [**a IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para recuperar los nombres de las otras vistas.</span><span class="sxs-lookup"><span data-stu-id="40e69-117">Call [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to retrieve the names of the other views.</span></span><br/> |
| [<span data-ttu-id="40e69-118">**GetViewTypeProperties**</span><span class="sxs-lookup"><span data-stu-id="40e69-118">**GetViewTypeProperties**</span></span>](ishellfolderviewtype-getviewtypeproperties.md) | <span data-ttu-id="40e69-119">Obtiene las propiedades de la vista.</span><span class="sxs-lookup"><span data-stu-id="40e69-119">Gets the properties of the view.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="40e69-120">**TranslateViewPidl**</span><span class="sxs-lookup"><span data-stu-id="40e69-120">**TranslateViewPidl**</span></span>](ishellfolderviewtype-translateviewpidl.md)         | <span data-ttu-id="40e69-121">Reconstruye un PIDL de una representación jerárquica de la carpeta Shell en una representación diferente.</span><span class="sxs-lookup"><span data-stu-id="40e69-121">Reconstructs a PIDL from one hierarchical representation of the Shell folder into a different representation.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="40e69-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40e69-122">Remarks</span></span>

<span data-ttu-id="40e69-123">Este enumerador devuelve PIDL que son carpetas ocultas especiales en el nivel superior de la carpeta Shell, que de lo contrario no se enumeran.</span><span class="sxs-lookup"><span data-stu-id="40e69-123">This enumerator returns PIDLs that are special hidden folders at the top level of the Shell folder, which are not otherwise enumerated.</span></span> <span data-ttu-id="40e69-124">La vista predeterminada es la que la carpeta shell muestra con normalidad.</span><span class="sxs-lookup"><span data-stu-id="40e69-124">The default view is the one the Shell folder displays normally.</span></span>

<span data-ttu-id="40e69-125">Esta interfaz no está definida en ningún archivo de encabezado público.</span><span class="sxs-lookup"><span data-stu-id="40e69-125">This interface is not defined in any public header file.</span></span> <span data-ttu-id="40e69-126">Si decide implementar esta interfaz, puede usar el siguiente código de C/C++ para declarar sus métodos.</span><span class="sxs-lookup"><span data-stu-id="40e69-126">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE   IShellFolderViewType
DECLARE_INTERFACE_IID_(IShellFolderViewType, IUnknown, "49422C1E-1C03-11d2-8DAB-0000F87A556C")
{
    // *** IUnknown methods ***
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void **ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // *** IShellFolderViewType Methods ***

    // EnumViews:
    //   Returns an enumerator which will give out one pidl for every extended view.
    STDMETHOD(EnumViews)(THIS_ ULONG grfFlags, __out IEnumIDList **ppenum) PURE;

    // GetDefaultViewName:
    //   Returns the name of the default view.  The names of the other views
    //   can be retrieved by calling GetDisplayNameOf.
    STDMETHOD(GetDefaultViewName)(THIS_ DWORD  uFlags, __out LPWSTR *ppwszName) PURE;
    STDMETHOD(GetViewTypeProperties)(THIS_ PCUITEMID_CHILD pidl, __out DWORD *pdwFlags)  PURE;

    // TranslateViewPidl:
    //   Attempts to take a pidl represented in one hierarchical representation of
    //   the Shell folder, and find it in a different representation.
    //   pidl should be relative to the root folder.
    //   Remember to ILFree ppidlOut
    STDMETHOD(TranslateViewPidl)(THIS_ PCUIDLIST_RELATIVE pidl, PCUIDLIST_RELATIVE pidlView,
              __out PIDLIST_RELATIVE *ppidlOut) PURE;
};

#define SFVTFLAG_NOTIFY_CREATE  0x00000001
#define SFVTFLAG_NOTIFY_RESORT  0x00000002
```



## <a name="requirements"></a><span data-ttu-id="40e69-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40e69-127">Requirements</span></span>



| <span data-ttu-id="40e69-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="40e69-128">Requirement</span></span> | <span data-ttu-id="40e69-129">Value</span><span class="sxs-lookup"><span data-stu-id="40e69-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40e69-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40e69-130">Minimum supported client</span></span><br/> | <span data-ttu-id="40e69-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="40e69-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="40e69-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40e69-132">Minimum supported server</span></span><br/> | <span data-ttu-id="40e69-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="40e69-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="40e69-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="40e69-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40e69-135"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40e69-135"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
