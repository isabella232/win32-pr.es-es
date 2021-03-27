---
description: 'Permite que el objeto de devolución de llamada especifique una cadena de texto de información sobre herramientas para los elementos de menú o botones de barra de herramientas. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: 29849218-0d30-4412-86c8-5d320bc5dd26
title: Mensaje de SFVM_GETTOOLTIPTEXT (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffea70f6051ec435e14640ac70d2e9617b11305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002981"
---
# <a name="sfvm_gettooltiptext-message"></a><span data-ttu-id="25f8f-104">SFVM \_ GETTOOLTIPTEXT</span><span class="sxs-lookup"><span data-stu-id="25f8f-104">SFVM\_GETTOOLTIPTEXT message</span></span>

<span data-ttu-id="25f8f-105">Permite que el objeto de devolución de llamada especifique una cadena de texto de información sobre herramientas para los elementos de menú o botones de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="25f8f-105">Allows the callback object to specify a tooltip text string for menu items or toolbar buttons.</span></span> <span data-ttu-id="25f8f-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="25f8f-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETTOOLTIPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="25f8f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25f8f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25f8f-108">*idCmd \_ cchMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="25f8f-108">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25f8f-109">La palabra de orden inferior de este parámetro contiene el identificador de comando.</span><span class="sxs-lookup"><span data-stu-id="25f8f-109">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="25f8f-110">La palabra de orden superior contiene el número de caracteres en el búfer de *miembros pszText* .</span><span class="sxs-lookup"><span data-stu-id="25f8f-110">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="25f8f-111">*miembros pszText* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="25f8f-111">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25f8f-112">Una cadena terminada en null que contiene el texto de ayuda.</span><span class="sxs-lookup"><span data-stu-id="25f8f-112">A null-terminated string containing the help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25f8f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25f8f-113">Requirements</span></span>



| <span data-ttu-id="25f8f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="25f8f-114">Requirement</span></span> | <span data-ttu-id="25f8f-115">Value</span><span class="sxs-lookup"><span data-stu-id="25f8f-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="25f8f-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25f8f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="25f8f-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="25f8f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="25f8f-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25f8f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="25f8f-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="25f8f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="25f8f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25f8f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="25f8f-121"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="25f8f-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
