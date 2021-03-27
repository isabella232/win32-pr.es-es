---
description: 'Notifica al objeto de devolución de llamada que el usuario ha haga clic en un encabezado de columna para ordenar la lista de objetos en la vista de carpetas. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_COLUMNCLICK (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 351be842-6ea5-4223-8162-0e6c4e6a5afb
api_name:
- SFVM_COLUMNCLICK
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bca80554e25378af1c078a36a02222390b771874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497890"
---
# <a name="sfvm_columnclick-message"></a><span data-ttu-id="b88d1-104">SFVM \_ COLUMNCLICK</span><span class="sxs-lookup"><span data-stu-id="b88d1-104">SFVM\_COLUMNCLICK message</span></span>

<span data-ttu-id="b88d1-105">Notifica al objeto de devolución de llamada que el usuario ha haga clic en un encabezado de columna para ordenar la lista de objetos en la vista de carpetas.</span><span class="sxs-lookup"><span data-stu-id="b88d1-105">Notifies the callback object that the user has clicked a column header to sort the list of objects in the folder view.</span></span> <span data-ttu-id="b88d1-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="b88d1-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_COLUMNCLICK 

    wParam = (WPARAM)(UINT)iColumn;

            
```



## <a name="parameters"></a><span data-ttu-id="b88d1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b88d1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b88d1-108">*iColumn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b88d1-108">*iColumn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b88d1-109">Índice de la columna en la que se hizo clic.</span><span class="sxs-lookup"><span data-stu-id="b88d1-109">The index of the column that was clicked.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b88d1-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b88d1-110">Remarks</span></span>

<span data-ttu-id="b88d1-111">En respuesta a esta notificación, debe devolver S \_ OK para reorganizar la lista.</span><span class="sxs-lookup"><span data-stu-id="b88d1-111">In response to this notification, you should return S\_OK to rearrange the list yourself.</span></span> <span data-ttu-id="b88d1-112">Para que el objeto de vista de carpeta del sistema reorganice la lista, devuelva S \_ false.</span><span class="sxs-lookup"><span data-stu-id="b88d1-112">To have the system folder view object rearrange the list, return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="b88d1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b88d1-113">Requirements</span></span>



| <span data-ttu-id="b88d1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b88d1-114">Requirement</span></span> | <span data-ttu-id="b88d1-115">Value</span><span class="sxs-lookup"><span data-stu-id="b88d1-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b88d1-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b88d1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b88d1-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b88d1-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b88d1-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b88d1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b88d1-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b88d1-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b88d1-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b88d1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b88d1-121"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="b88d1-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
