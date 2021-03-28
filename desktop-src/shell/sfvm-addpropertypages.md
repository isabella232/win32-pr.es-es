---
description: 'Permite que el objeto de devolución de llamada proporcione una página que se va a agregar a la hoja de propiedades propiedades del objeto seleccionado. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_ADDPROPERTYPAGES (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 54f67d0e-6089-4e75-a547-5313794e1512
api_name:
- SFVM_ADDPROPERTYPAGES
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5f3e1f39b457bce105a8ac2b4be8b5939435615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997809"
---
# <a name="sfvm_addpropertypages-message"></a><span data-ttu-id="c495c-104">SFVM \_ ADDPROPERTYPAGES</span><span class="sxs-lookup"><span data-stu-id="c495c-104">SFVM\_ADDPROPERTYPAGES message</span></span>

<span data-ttu-id="c495c-105">Permite que el objeto de devolución de llamada proporcione una página que se va a agregar a la hoja de propiedades **propiedades** del objeto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="c495c-105">Allows the callback object to provide a page to add to the **Properties** property sheet of the selected object.</span></span> <span data-ttu-id="c495c-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="c495c-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_ADDPROPERTYPAGES 

    lParam = (LPARAM)(SFVM_PROPPAGE_DATA*) pData;

            
```



## <a name="parameters"></a><span data-ttu-id="c495c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c495c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c495c-108">*pdata* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c495c-108">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c495c-109">La dirección de una estructura de [**\_ \_ datos de SFVM PROPPAGE**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data) .</span><span class="sxs-lookup"><span data-stu-id="c495c-109">The address of a [**SFVM\_PROPPAGE\_DATA**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c495c-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c495c-110">Remarks</span></span>

<span data-ttu-id="c495c-111">Este mensaje sirve esencialmente la misma función que [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span><span class="sxs-lookup"><span data-stu-id="c495c-111">This message serves essentially the same function as [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span></span> <span data-ttu-id="c495c-112">Vea [crear controladores de hoja de propiedades](propsheet-handlers.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c495c-112">See [Creating Property Sheet Handlers](propsheet-handlers.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="c495c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c495c-113">Requirements</span></span>



| <span data-ttu-id="c495c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c495c-114">Requirement</span></span> | <span data-ttu-id="c495c-115">Value</span><span class="sxs-lookup"><span data-stu-id="c495c-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c495c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c495c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c495c-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c495c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c495c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c495c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c495c-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c495c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c495c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c495c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c495c-121"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="c495c-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
