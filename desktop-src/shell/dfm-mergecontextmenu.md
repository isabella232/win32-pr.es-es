---
description: Permite que la devolución de llamada agregue elementos al menú.
title: Mensaje de DFM_MERGECONTEXTMENU (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2fd779ac-7dd6-4b81-86dc-8930db27ae59
api_name:
- DFM_MERGECONTEXTMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d469f9764b5e377e5f47227d3414f246441d3505
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984298"
---
# <a name="dfm_mergecontextmenu-message"></a><span data-ttu-id="21c74-103">DFM \_ MERGECONTEXTMENU</span><span class="sxs-lookup"><span data-stu-id="21c74-103">DFM\_MERGECONTEXTMENU message</span></span>

<span data-ttu-id="21c74-104">Permite que la devolución de llamada agregue elementos al menú.</span><span class="sxs-lookup"><span data-stu-id="21c74-104">Allows the callback to add items to the menu.</span></span>


```C++
DFM_MERGECONTEXTMENU

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a><span data-ttu-id="21c74-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21c74-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21c74-106">*pqcminfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21c74-106">*pqcminfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21c74-107">Puntero a una estructura [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) que contiene la información utilizada en la combinación.</span><span class="sxs-lookup"><span data-stu-id="21c74-107">A pointer to a [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) structure containing the information used in the merge.</span></span>

</dd> <dt>

<span data-ttu-id="21c74-108">*uFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21c74-108">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21c74-109">Marcas que especifican cómo se puede cambiar el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="21c74-109">Flags specifying how the context menu can be changed.</span></span> <span data-ttu-id="21c74-110">Este parámetro usa los \_ \* valores CMF descritos en [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span><span class="sxs-lookup"><span data-stu-id="21c74-110">This parameter uses the CMF\_\* values described in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21c74-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21c74-111">Remarks</span></span>

<span data-ttu-id="21c74-112">Si los elementos se agregan al menú contextual, deben ser compatibles con rutinas que respondan correctamente cuando se invoque uno de esos elementos mediante [**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md).</span><span class="sxs-lookup"><span data-stu-id="21c74-112">If items are added to the context menu, they must be supported with routines that respond appropriately when one of those items is invoked using [**DFM\_INVOKECOMMAND**](dfm-invokecommand.md).</span></span>

<span data-ttu-id="21c74-113">Este mensaje se envía a la función de devolución de llamada o al objeto de devolución de llamada, dependiendo de cómo se implemente el objeto de menú contextual predeterminado.</span><span class="sxs-lookup"><span data-stu-id="21c74-113">This message is sent to either the callback function or the callback object depending on how the default context menu object is implemented.</span></span> <span data-ttu-id="21c74-114">Hay dos API para su implementación, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="21c74-114">There are two APIs for its implementation, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="21c74-115">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) es una versión extendida de este mensaje y proporciona más información a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="21c74-115">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="21c74-116">Use **DFM \_ INVOKECOMMANDEX** si necesita la información adicional proporcionada por esa interfaz en su implementación de.</span><span class="sxs-lookup"><span data-stu-id="21c74-116">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="21c74-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21c74-117">Requirements</span></span>



| <span data-ttu-id="21c74-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="21c74-118">Requirement</span></span> | <span data-ttu-id="21c74-119">Value</span><span class="sxs-lookup"><span data-stu-id="21c74-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="21c74-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21c74-120">Minimum supported client</span></span><br/> | <span data-ttu-id="21c74-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="21c74-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="21c74-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21c74-122">Minimum supported server</span></span><br/> | <span data-ttu-id="21c74-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="21c74-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="21c74-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21c74-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="21c74-125"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="21c74-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




