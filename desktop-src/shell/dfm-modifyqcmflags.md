---
description: 'Permite que la devolución de llamada modifique los valores de CFM \_ XXX pasados a IContextMenu:: QueryContextMenu.'
title: Mensaje de DFM_MODIFYQCMFLAGS (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2c87e14d-4cf4-425d-a5fe-9dc7530f0e59
api_name:
- DFM_MODIFYQCMFLAGS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ff90cfb0e0297e7d3276f00f314fce865920663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907727"
---
# <a name="dfm_modifyqcmflags-message"></a><span data-ttu-id="72d74-103">DFM \_ MODIFYQCMFLAGS</span><span class="sxs-lookup"><span data-stu-id="72d74-103">DFM\_MODIFYQCMFLAGS message</span></span>

<span data-ttu-id="72d74-104">Permite que la devolución de llamada modifique los valores de CFM \_ XXX pasados a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span><span class="sxs-lookup"><span data-stu-id="72d74-104">Allows the callback to modify the CFM\_XXX values passed to [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>


```C++
DFM_MODIFYQCMFLAGS

    lParam = (LPARAM)(UINT) *puNewFlags;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a><span data-ttu-id="72d74-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72d74-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72d74-106">*puNewFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="72d74-106">*puNewFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72d74-107">Puntero a los nuevos valores de marca.</span><span class="sxs-lookup"><span data-stu-id="72d74-107">A pointer to the new flag values.</span></span>

</dd> <dt>

<span data-ttu-id="72d74-108">*uFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="72d74-108">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72d74-109">Marcas que especifican cómo se puede cambiar el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="72d74-109">Flags that specify how the context menu can be changed.</span></span> <span data-ttu-id="72d74-110">Este parámetro usa los \_ valores de CMF XXX descritos en [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span><span class="sxs-lookup"><span data-stu-id="72d74-110">This parameter uses the CMF\_XXX values described in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72d74-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72d74-111">Requirements</span></span>



| <span data-ttu-id="72d74-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="72d74-112">Requirement</span></span> | <span data-ttu-id="72d74-113">Value</span><span class="sxs-lookup"><span data-stu-id="72d74-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="72d74-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72d74-114">Minimum supported client</span></span><br/> | <span data-ttu-id="72d74-115">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="72d74-115">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="72d74-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72d74-116">Minimum supported server</span></span><br/> | <span data-ttu-id="72d74-117">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="72d74-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="72d74-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72d74-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="72d74-119"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="72d74-119"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




