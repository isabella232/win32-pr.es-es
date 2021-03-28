---
description: 'Notifica al objeto de devolución de llamada que el usuario ha invocado uno de sus comandos de menú o barra de herramientas. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: 6b9e4a4d-ec45-489c-bbff-d123d5756b75
title: Mensaje de SFVM_INVOKECOMMAND (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5fc9709827250e5cf8060400bbecb714ae5998
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913313"
---
# <a name="sfvm_invokecommand-message"></a><span data-ttu-id="bb8cb-104">SFVM \_ INVOKECOMMAND</span><span class="sxs-lookup"><span data-stu-id="bb8cb-104">SFVM\_INVOKECOMMAND message</span></span>

<span data-ttu-id="bb8cb-105">Notifica al objeto de devolución de llamada que el usuario ha invocado uno de sus comandos de menú o barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bb8cb-105">Notifies the callback object that one of its toolbar or menu commands has been invoked by the user.</span></span> <span data-ttu-id="bb8cb-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="bb8cb-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_INVOKECOMMAND 

    wParam = (WPARAM)(UINT) idCmd;

            
```



## <a name="parameters"></a><span data-ttu-id="bb8cb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb8cb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb8cb-108">*idCmd* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="bb8cb-108">*idCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb8cb-109">IDENTIFICADOR de comando de la barra de herramientas o el elemento de menú seleccionado.</span><span class="sxs-lookup"><span data-stu-id="bb8cb-109">The command ID of the selected toolbar or menu item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb8cb-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb8cb-110">Remarks</span></span>

<span data-ttu-id="bb8cb-111">Este mensaje sirve esencialmente la misma función que un mensaje de [**\_ comando de WM**](../menurc/wm-command.md) en un procedimiento de ventana convencional.</span><span class="sxs-lookup"><span data-stu-id="bb8cb-111">This message serves essentially the same function as a [**WM\_COMMAND**](../menurc/wm-command.md) message in a conventional window procedure.</span></span> <span data-ttu-id="bb8cb-112">Permite que el objeto de devolución de llamada controle los elementos que ha agregado a la herramienta explorador de Windows o a la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="bb8cb-112">It allows the callback object to handle any items that it has added to the Windows Explorer tool or menu bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb8cb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb8cb-113">Requirements</span></span>



| <span data-ttu-id="bb8cb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb8cb-114">Requirement</span></span> | <span data-ttu-id="bb8cb-115">Value</span><span class="sxs-lookup"><span data-stu-id="bb8cb-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bb8cb-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb8cb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bb8cb-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bb8cb-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bb8cb-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb8cb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bb8cb-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bb8cb-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bb8cb-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb8cb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb8cb-121"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb8cb-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
