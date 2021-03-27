---
description: 'Permite que el objeto de devolución de llamada especifique una cadena de texto de ayuda para los elementos de menú o los botones de la barra de herramientas. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_GETHELPTEXT (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9bd6d632-308c-4ba5-8ac6-2d0f65853947
api_name:
- SFVM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5b33bd99c2dd1e6d1013da9015a5ff70bc111c79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815478"
---
# <a name="sfvm_gethelptext-message"></a><span data-ttu-id="36448-104">SFVM \_ GETHELPTEXT</span><span class="sxs-lookup"><span data-stu-id="36448-104">SFVM\_GETHELPTEXT message</span></span>

<span data-ttu-id="36448-105">Permite que el objeto de devolución de llamada especifique una cadena de texto de ayuda para los elementos de menú o los botones de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="36448-105">Allows the callback object to specify a help text string for menu items or toolbar buttons.</span></span> <span data-ttu-id="36448-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="36448-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="36448-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36448-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36448-108">*idCmd \_ cchMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="36448-108">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36448-109">La palabra de orden inferior de este parámetro contiene el identificador de comando.</span><span class="sxs-lookup"><span data-stu-id="36448-109">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="36448-110">La palabra de orden superior contiene el número de caracteres en el búfer de *miembros pszText* .</span><span class="sxs-lookup"><span data-stu-id="36448-110">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="36448-111">*miembros pszText* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="36448-111">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36448-112">Una cadena terminada en null que contiene el texto de ayuda.</span><span class="sxs-lookup"><span data-stu-id="36448-112">A null-terminated string containing the help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36448-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36448-113">Requirements</span></span>



| <span data-ttu-id="36448-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="36448-114">Requirement</span></span> | <span data-ttu-id="36448-115">Value</span><span class="sxs-lookup"><span data-stu-id="36448-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="36448-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36448-116">Minimum supported client</span></span><br/> | <span data-ttu-id="36448-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="36448-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="36448-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36448-118">Minimum supported server</span></span><br/> | <span data-ttu-id="36448-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="36448-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="36448-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36448-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="36448-121"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="36448-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
