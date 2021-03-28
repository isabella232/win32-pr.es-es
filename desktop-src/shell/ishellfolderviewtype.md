---
description: Expone métodos que permiten que una carpeta de Shell admita vistas diferentes en su contenido (diferentes diseños jerárquicos de sus datos).
title: Interfaz IShellFolderViewType
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
ms.openlocfilehash: 1440b6d14950ad70d2c76168b28bb1077b19b5a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082632"
---
# <a name="ishellfolderviewtype-interface"></a><span data-ttu-id="697f6-103">Interfaz IShellFolderViewType</span><span class="sxs-lookup"><span data-stu-id="697f6-103">IShellFolderViewType interface</span></span>

<span data-ttu-id="697f6-104">Expone métodos que permiten que una carpeta de Shell admita vistas diferentes en su contenido (diferentes diseños jerárquicos de sus datos).</span><span class="sxs-lookup"><span data-stu-id="697f6-104">Exposes methods that enable a Shell folder to support different views on its content (different hierarchical layouts of its data).</span></span>

## <a name="members"></a><span data-ttu-id="697f6-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="697f6-105">Members</span></span>

<span data-ttu-id="697f6-106">La interfaz **IShellFolderViewType** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="697f6-106">The **IShellFolderViewType** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="697f6-107">**IShellFolderViewType** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="697f6-107">**IShellFolderViewType** also has these types of members:</span></span>

-   [<span data-ttu-id="697f6-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="697f6-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="697f6-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="697f6-109">Methods</span></span>

<span data-ttu-id="697f6-110">La interfaz **IShellFolderViewType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="697f6-110">The **IShellFolderViewType** interface has these methods.</span></span>



| <span data-ttu-id="697f6-111">Método</span><span class="sxs-lookup"><span data-stu-id="697f6-111">Method</span></span>                                                                      | <span data-ttu-id="697f6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="697f6-112">Description</span></span>                                                                                                                                                          |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="697f6-113">**EnumViews**</span><span class="sxs-lookup"><span data-stu-id="697f6-113">**EnumViews**</span></span>](ishellfolderviewtype-enumviews.md)                         | <span data-ttu-id="697f6-114">Recupera un enumerador que devolverá un PIDL para cada vista extendida.</span><span class="sxs-lookup"><span data-stu-id="697f6-114">Retrieves an enumerator that will return one PIDL for every extended view.</span></span><br/>                                                                                |
| [<span data-ttu-id="697f6-115">**GetDefaultViewName**</span><span class="sxs-lookup"><span data-stu-id="697f6-115">**GetDefaultViewName**</span></span>](ishellfolderviewtype-getdefaultviewname.md)       | <span data-ttu-id="697f6-116">Obtiene el nombre de la vista predeterminada.</span><span class="sxs-lookup"><span data-stu-id="697f6-116">Gets the name of the default view.</span></span> <span data-ttu-id="697f6-117">Llame a [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para recuperar los nombres de las otras vistas.</span><span class="sxs-lookup"><span data-stu-id="697f6-117">Call [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to retrieve the names of the other views.</span></span><br/> |
| [<span data-ttu-id="697f6-118">**GetViewTypeProperties**</span><span class="sxs-lookup"><span data-stu-id="697f6-118">**GetViewTypeProperties**</span></span>](ishellfolderviewtype-getviewtypeproperties.md) | <span data-ttu-id="697f6-119">Obtiene las propiedades de la vista.</span><span class="sxs-lookup"><span data-stu-id="697f6-119">Gets the properties of the view.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="697f6-120">**TranslateViewPidl**</span><span class="sxs-lookup"><span data-stu-id="697f6-120">**TranslateViewPidl**</span></span>](ishellfolderviewtype-translateviewpidl.md)         | <span data-ttu-id="697f6-121">Reconstruye un PIDL a partir de una representación jerárquica de la carpeta de Shell en una representación diferente.</span><span class="sxs-lookup"><span data-stu-id="697f6-121">Reconstructs a PIDL from one hierarchical representation of the Shell folder into a different representation.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="697f6-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="697f6-122">Remarks</span></span>

<span data-ttu-id="697f6-123">Este enumerador devuelve PIDL que son carpetas ocultas especiales en el nivel superior de la carpeta de Shell, que no se enumeran de otra manera.</span><span class="sxs-lookup"><span data-stu-id="697f6-123">This enumerator returns PIDLs that are special hidden folders at the top level of the Shell folder, which are not otherwise enumerated.</span></span> <span data-ttu-id="697f6-124">La vista predeterminada es la que la carpeta de Shell muestra con normalidad.</span><span class="sxs-lookup"><span data-stu-id="697f6-124">The default view is the one the Shell folder displays normally.</span></span>

<span data-ttu-id="697f6-125">Esta interfaz no está definida en ningún archivo de encabezado público.</span><span class="sxs-lookup"><span data-stu-id="697f6-125">This interface is not defined in any public header file.</span></span> <span data-ttu-id="697f6-126">Si decide implementar esta interfaz, puede usar el siguiente código de C/C++ para declarar sus métodos.</span><span class="sxs-lookup"><span data-stu-id="697f6-126">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE   IShellFolderViewType
DECLARE_INTERFACE_IID_(IShellFolderViewType, IUnknown, "49422C1E-1C03-11d2-8DAB-0000F87A556C")
{
    // **_ IUnknown methods _*_
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void _*ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // **_ IShellFolderViewType Methods _*_

    // EnumViews:
    //   Returns an enumerator which will give out one pidl for every extended view.
    STDMETHOD(EnumViews)(THIS_ ULONG grfFlags, __out IEnumIDList _*ppenum) PURE;

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



## <a name="requirements"></a><span data-ttu-id="697f6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="697f6-127">Requirements</span></span>



| <span data-ttu-id="697f6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="697f6-128">Requirement</span></span> | <span data-ttu-id="697f6-129">Value</span><span class="sxs-lookup"><span data-stu-id="697f6-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="697f6-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="697f6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="697f6-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="697f6-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="697f6-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="697f6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="697f6-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="697f6-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="697f6-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="697f6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="697f6-135"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="697f6-135"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
