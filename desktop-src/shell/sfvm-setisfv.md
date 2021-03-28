---
description: 'Notifica el objeto de devolución de llamada del sitio del contenedor. Solo se usa cuando no se admite IObjectWithSite:: SetSite y se usa SHCreateShellFolderViewEx. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: a4aa40f8-1d98-4686-86e2-87280e470aac
title: Mensaje de SFVM_SETISFV (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83021f1d6d52286f08e8ec7bd51bbaa806c17c7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986099"
---
# <a name="sfvm_setisfv-message"></a><span data-ttu-id="01ef0-105">SFVM \_ SETISFV</span><span class="sxs-lookup"><span data-stu-id="01ef0-105">SFVM\_SETISFV message</span></span>

<span data-ttu-id="01ef0-106">\[Esta notificación se admite a través de Windows XP Service Pack 2 (SP2) y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="01ef0-106">\[This notification is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="01ef0-107">Es posible que no se admita en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="01ef0-107">It might be unsupported in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="01ef0-108">Notifica el objeto de devolución de llamada del sitio del contenedor.</span><span class="sxs-lookup"><span data-stu-id="01ef0-108">Notifies the callback object of the container site.</span></span> <span data-ttu-id="01ef0-109">Solo se usa cuando no se admite [**IObjectWithSite:: SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) y se usa [**SHCreateShellFolderViewEx**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) .</span><span class="sxs-lookup"><span data-stu-id="01ef0-109">This is used only when [**IObjectWithSite::SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) is not supported and [**SHCreateShellFolderViewEx**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) is used.</span></span> <span data-ttu-id="01ef0-110">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="01ef0-110">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_SETISFV
    lParam = (LPARAM)(IUnknown*) site;
            
```



## <a name="parameters"></a><span data-ttu-id="01ef0-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01ef0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01ef0-112">*sitio* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="01ef0-112">*site* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01ef0-113">Puntero a la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del sitio del contenedor.</span><span class="sxs-lookup"><span data-stu-id="01ef0-113">A pointer to the container site's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01ef0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01ef0-114">Requirements</span></span>



| <span data-ttu-id="01ef0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="01ef0-115">Requirement</span></span> | <span data-ttu-id="01ef0-116">Value</span><span class="sxs-lookup"><span data-stu-id="01ef0-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="01ef0-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01ef0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="01ef0-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="01ef0-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="01ef0-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01ef0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="01ef0-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="01ef0-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="01ef0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01ef0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="01ef0-122"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="01ef0-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
