---
title: CFSTR_DSOP_DS_SELECTION_LIST (objsel. h)
description: El \_ formato del \_ portapapeles de la lista de selección DS de CFSTR DSOP \_ \_ proporciona un hglobal que contiene una estructura de lista de selección de DS \_ \_ . La estructura de la \_ lista de selección \_ de DS contiene datos sobre los elementos seleccionados en el cuadro de diálogo Selector de objetos de directorio.
ms.assetid: cd634e3b-0eb7-4144-b9e1-1d27a322f72c
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSOP_DS_SELECTION_LIST
api_location:
- Objsel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b783b0790ed87a292cd171cb8283333d5b9bd5b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996231"
---
# <a name="cfstr_dsop_ds_selection_list"></a><span data-ttu-id="9a4b6-104">CFSTR \_ DSOP \_ \_ lista de selección DS \_</span><span class="sxs-lookup"><span data-stu-id="9a4b6-104">CFSTR\_DSOP\_DS\_SELECTION\_LIST</span></span>

<dl> <dt>

<span data-ttu-id="9a4b6-105"><span id="CFSTR_DSOP_DS_SELECTION_LIST"></span><span id="cfstr_dsop_ds_selection_list"></span>**CFSTR \_ DSOP \_ \_ lista de selección DS \_**</span><span class="sxs-lookup"><span data-stu-id="9a4b6-105"><span id="CFSTR_DSOP_DS_SELECTION_LIST"></span><span id="cfstr_dsop_ds_selection_list"></span>**CFSTR\_DSOP\_DS\_SELECTION\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a4b6-106">"CFSTR \_ DSOP \_ DS \_ Selection \_ List"</span><span class="sxs-lookup"><span data-stu-id="9a4b6-106">"CFSTR\_DSOP\_DS\_SELECTION\_LIST"</span></span>
</dt> <dt>



<span data-ttu-id="9a4b6-107">El formato del portapapeles de la **lista de \_ \_ \_ selección \_ DS CFSTR DSOP** se proporciona [**mediante la llamada**](/windows/win32/api/objidl/nn-objidl-idataobject) a [**IDsObjectPicker:: InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog).</span><span class="sxs-lookup"><span data-stu-id="9a4b6-107">The **CFSTR\_DSOP\_DS\_SELECTION\_LIST** clipboard format is provided by the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) obtained by calling [**IDsObjectPicker::InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog).</span></span> <span data-ttu-id="9a4b6-108">El formato del portapapeles de la **\_ \_ \_ \_ lista de selección DS de CFSTR DSOP** proporciona un **HGLOBAL** que contiene una estructura de [**lista de \_ selección \_ de DS**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) .</span><span class="sxs-lookup"><span data-stu-id="9a4b6-108">The **CFSTR\_DSOP\_DS\_SELECTION\_LIST** clipboard format provides an **HGLOBAL** that contains a [**DS\_SELECTION\_LIST**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) structure.</span></span> <span data-ttu-id="9a4b6-109">La estructura de la **\_ \_ lista de selección de DS** contiene datos sobre los elementos seleccionados en el cuadro de diálogo Selector de objetos de [directorio](directory-object-picker.md) .</span><span class="sxs-lookup"><span data-stu-id="9a4b6-109">The **DS\_SELECTION\_LIST** structure contains data about the items selected in a [Directory Object Picker](directory-object-picker.md) dialog box.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9a4b6-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a4b6-110">Requirements</span></span>



| <span data-ttu-id="9a4b6-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a4b6-111">Requirement</span></span> | <span data-ttu-id="9a4b6-112">Value</span><span class="sxs-lookup"><span data-stu-id="9a4b6-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9a4b6-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a4b6-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9a4b6-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a4b6-114">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="9a4b6-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a4b6-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9a4b6-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a4b6-116">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="9a4b6-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a4b6-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a4b6-118"><dt>Objsel. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a4b6-118"><dt>Objsel.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a4b6-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a4b6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a4b6-120">**\_lista de selección de DS \_**</span><span class="sxs-lookup"><span data-stu-id="9a4b6-120">**DS\_SELECTION\_LIST**</span></span>](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list)
</dt> <dt>

[<span data-ttu-id="9a4b6-121">**IDsObjectPicker::InvokeDialog**</span><span class="sxs-lookup"><span data-stu-id="9a4b6-121">**IDsObjectPicker::InvokeDialog**</span></span>](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog)
</dt> <dt>

[<span data-ttu-id="9a4b6-122">Selector de objetos de directorio</span><span class="sxs-lookup"><span data-stu-id="9a4b6-122">Directory Object Picker</span></span>](directory-object-picker.md)
</dt> </dl>

 

