---
description: 'Permite que el objeto de devolución de llamada Combine los elementos de menú en los menús del explorador de Windows. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_MERGEMENU (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59bb99a3-9a5a-4ea5-9830-b04d7d886b3f
api_name:
- SFVM_MERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5cf95a7576c15ab1c3e64ebe55e244feffa6d86d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986075"
---
# <a name="sfvm_mergemenu-message"></a><span data-ttu-id="0bb0f-104">SFVM \_ MERGEMENU</span><span class="sxs-lookup"><span data-stu-id="0bb0f-104">SFVM\_MERGEMENU message</span></span>

<span data-ttu-id="0bb0f-105">Permite que el objeto de devolución de llamada Combine los elementos de menú en los menús del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="0bb0f-105">Allows the callback object to merge menu items into the Windows Explorer menus.</span></span> <span data-ttu-id="0bb0f-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="0bb0f-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_MERGEMENU 

    lParam = (LPARAM)(LPQCMINFO) pInfo;

            
```



## <a name="parameters"></a><span data-ttu-id="0bb0f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0bb0f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bb0f-108">*Pinfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0bb0f-108">*pInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bb0f-109">Estructura [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) que contiene la información necesaria para combinar los elementos en el menú.</span><span class="sxs-lookup"><span data-stu-id="0bb0f-109">A [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) structure containing the information needed to merge the items into the menu.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0bb0f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0bb0f-110">Remarks</span></span>

<span data-ttu-id="0bb0f-111">Este mensaje sirve esencialmente el mismo propósito que [**IShellBrowser:: InsertMenusSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) y [**IShellBrowser:: SetMenuSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) en una vista de carpeta personalizada.</span><span class="sxs-lookup"><span data-stu-id="0bb0f-111">This message serves essentially the same purpose as the [**IShellBrowser::InsertMenusSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) and [**IShellBrowser::SetMenuSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) in a custom folder view.</span></span> <span data-ttu-id="0bb0f-112">Vea la sección *uso de IShellBrowser para comunicarse con el explorador de Windows* de implementación de [una vista de carpeta](../lwef/nse-folderview.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="0bb0f-112">See the *Using IShellBrowser to Communicate with Windows Explorer* section of [Implementing a Folder View](../lwef/nse-folderview.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bb0f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bb0f-113">Requirements</span></span>



| <span data-ttu-id="0bb0f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bb0f-114">Requirement</span></span> | <span data-ttu-id="0bb0f-115">Value</span><span class="sxs-lookup"><span data-stu-id="0bb0f-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0bb0f-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0bb0f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0bb0f-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0bb0f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0bb0f-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0bb0f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0bb0f-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0bb0f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0bb0f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0bb0f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bb0f-121"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bb0f-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
