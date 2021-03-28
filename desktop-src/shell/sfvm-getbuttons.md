---
description: 'Permite que el objeto de devolución de llamada especifique los botones que se van a agregar a la barra de herramientas. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: 0c0dbf61-9da9-4bcc-bad9-92c3f78db78f
title: Mensaje de SFVM_GETBUTTONS (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ad4ced86909c37ec77bf0470b46a40954f5b61c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911398"
---
# <a name="sfvm_getbuttons-message"></a><span data-ttu-id="7e89f-104">SFVM \_ GETBUTTONS</span><span class="sxs-lookup"><span data-stu-id="7e89f-104">SFVM\_GETBUTTONS message</span></span>

<span data-ttu-id="7e89f-105">Permite que el objeto de devolución de llamada especifique los botones que se van a agregar a la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="7e89f-105">Allows the callback object to specify the buttons to be added to the toolbar.</span></span> <span data-ttu-id="7e89f-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="7e89f-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETBUTTONS 

    wParam = (WPARAM)(DWORD) idCmdFirst,cbtnMax;

    lParam = (LPARAM)(LPTBBUTTON) pbtn;

            
```



## <a name="parameters"></a><span data-ttu-id="7e89f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e89f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e89f-108">*idCmdFirst \_ cbtnMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="7e89f-108">*idCmdFirst\_cbtnMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e89f-109">Contiene los valores de 2 16 bits empaquetados en el parámetro con la macro [**MAKEWPARAM**](/windows/win32/api/winuser/nf-winuser-makewparam) .</span><span class="sxs-lookup"><span data-stu-id="7e89f-109">Contains two 16-bit values packed into the parameter with the [**MAKEWPARAM**](/windows/win32/api/winuser/nf-winuser-makewparam) macro.</span></span> <span data-ttu-id="7e89f-110">La palabra de orden inferior contiene el identificador de comando inicial.</span><span class="sxs-lookup"><span data-stu-id="7e89f-110">The low-order word contains the initial command ID.</span></span> <span data-ttu-id="7e89f-111">La palabra de orden superior contiene el número de botones que se van a agregar, tal como se especifica en el mensaje [**SFVM \_ GETBUTTONINFO**](sfvm-getbuttoninfo.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="7e89f-111">The high-order word contains the number of buttons to be added, as specified in the preceding [**SFVM\_GETBUTTONINFO**](sfvm-getbuttoninfo.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="7e89f-112">*pbtn* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7e89f-112">*pbtn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e89f-113">La dirección de una matriz de estructuras [**TBBUTTON**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) , una para cada botón que se va a agregar a la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="7e89f-113">The address of an array of [**TBBUTTON**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) structures, one for each button to be added to the toolbar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e89f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e89f-114">Remarks</span></span>

<span data-ttu-id="7e89f-115">Este mensaje está precedido por un mensaje [**SFVM \_ GETBUTTONINFO**](sfvm-getbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="7e89f-115">This message is preceded by a [**SFVM\_GETBUTTONINFO**](sfvm-getbuttoninfo.md) message.</span></span> <span data-ttu-id="7e89f-116">El objeto de devolución de llamada debe controlar ese mensaje para especificar el número de botones y dónde se colocarán en la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="7e89f-116">The callback object must handle that message to specify the number of buttons and where they are to be placed on the toolbar.</span></span> <span data-ttu-id="7e89f-117">En función de cómo responda el objeto de devolución de llamada al mensaje **\_ GETBUTTONINFO de SFVM** , los botones especificados por el parámetro *pbtn* se anexarán o anteponerán a los botones estándar del objeto de vista de carpeta del sistema, o se reemplazarán al conjunto estándar.</span><span class="sxs-lookup"><span data-stu-id="7e89f-117">Depending on how the callback object responds to the **SFVM\_GETBUTTONINFO** message, the buttons specified by *pbtn* parameter will be appended or prepended to the system folder view object's standard buttons, or replace the standard set.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e89f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e89f-118">Requirements</span></span>



| <span data-ttu-id="7e89f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e89f-119">Requirement</span></span> | <span data-ttu-id="7e89f-120">Value</span><span class="sxs-lookup"><span data-stu-id="7e89f-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7e89f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e89f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7e89f-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7e89f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7e89f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e89f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7e89f-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7e89f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7e89f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e89f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e89f-126"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e89f-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
