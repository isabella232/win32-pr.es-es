---
description: 'Permite que el objeto de devolución de llamada agregue botones a la barra de herramientas. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_GETBUTTONINFO (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 983652ed-7309-46aa-a6c9-7516411ba5ac
api_name:
- SFVM_GETBUTTONINFO
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d0db40f7c1f54cd13d54765ba34a8eab31246809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985774"
---
# <a name="sfvm_getbuttoninfo-message"></a><span data-ttu-id="d7969-104">SFVM \_ GETBUTTONINFO</span><span class="sxs-lookup"><span data-stu-id="d7969-104">SFVM\_GETBUTTONINFO message</span></span>

<span data-ttu-id="d7969-105">Permite que el objeto de devolución de llamada agregue botones a la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="d7969-105">Allows the callback object to add buttons to the toolbar.</span></span> <span data-ttu-id="d7969-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="d7969-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETBUTTONINFO 

    lParam = (LPARAM)(LPTBINFO) ptbinfo;

            
```



## <a name="parameters"></a><span data-ttu-id="d7969-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7969-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7969-108">*ptbinfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d7969-108">*ptbinfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7969-109">Dirección de una estructura [**TBINFO**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo) que especifica el número de botones y cómo se van a agregar a la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="d7969-109">The address of a [**TBINFO**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo) structure that specifies the number of buttons and how they are to be added to the toolbar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7969-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7969-110">Remarks</span></span>

<span data-ttu-id="d7969-111">Los botones se pueden anexar o anteponer a los botones de objeto de vista de carpeta del sistema estándar, o bien se pueden mostrar en lugar de los botones estándar.</span><span class="sxs-lookup"><span data-stu-id="d7969-111">Buttons can be appended or prepended to the standard system folder view object buttons, or be displayed in place of the standard buttons.</span></span> <span data-ttu-id="d7969-112">Este mensaje va seguido de un mensaje de [**SFVM \_ GETBUTTONS**](sfvm-getbuttons.md) que recupera la información relativa a los detalles del botón.</span><span class="sxs-lookup"><span data-stu-id="d7969-112">This message is followed by a [**SFVM\_GETBUTTONS**](sfvm-getbuttons.md) message that retrieves the information concerning the button specifics.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7969-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7969-113">Requirements</span></span>



| <span data-ttu-id="d7969-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7969-114">Requirement</span></span> | <span data-ttu-id="d7969-115">Value</span><span class="sxs-lookup"><span data-stu-id="d7969-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d7969-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7969-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d7969-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d7969-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d7969-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7969-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d7969-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d7969-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d7969-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7969-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7969-121"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7969-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
