---
description: Permite que el objeto de devolución de llamada especifique una cadena de texto de ayuda.
title: Mensaje de DFM_GETHELPTEXT (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 40ed981b-6d03-4c4f-9e70-1a01d49edcb0
api_name:
- DFM_GETHELPTEXT
- DFM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b9aefb1c3a12ff00294ccc536464794a17fccfc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540510"
---
# <a name="dfm_gethelptext-message"></a><span data-ttu-id="f633d-103">DFM \_ GETHELPTEXT</span><span class="sxs-lookup"><span data-stu-id="f633d-103">DFM\_GETHELPTEXT message</span></span>

<span data-ttu-id="f633d-104">Permite que el objeto de devolución de llamada especifique una cadena de texto de ayuda.</span><span class="sxs-lookup"><span data-stu-id="f633d-104">Allows the callback object to specify a help text string.</span></span>


```C++
DFM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="f633d-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f633d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f633d-106">*idCmd \_ cchMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="f633d-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f633d-107">La palabra de orden inferior de este parámetro contiene el identificador de comando.</span><span class="sxs-lookup"><span data-stu-id="f633d-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="f633d-108">La palabra de orden superior contiene el número de caracteres en el búfer de *miembros pszText* .</span><span class="sxs-lookup"><span data-stu-id="f633d-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f633d-109">*miembros pszText* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f633d-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f633d-110">Una cadena ANSI terminada en null que contiene el texto de ayuda.</span><span class="sxs-lookup"><span data-stu-id="f633d-110">A null-terminated ANSI string containing the help text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f633d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f633d-111">Remarks</span></span>

<span data-ttu-id="f633d-112">Este mensaje se envía a la función de devolución de llamada o al objeto de devolución de llamada, dependiendo de cómo se construya el objeto de menú contextual predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f633d-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="f633d-113">Hay dos API para su construcción, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="f633d-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="f633d-114">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) es una versión extendida de este mensaje y proporciona más información a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="f633d-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="f633d-115">Use **DFM \_ INVOKECOMMANDEX** si necesita la información adicional proporcionada por esa interfaz en su implementación de.</span><span class="sxs-lookup"><span data-stu-id="f633d-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="f633d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f633d-116">Requirements</span></span>



| <span data-ttu-id="f633d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f633d-117">Requirement</span></span> | <span data-ttu-id="f633d-118">Value</span><span class="sxs-lookup"><span data-stu-id="f633d-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f633d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f633d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f633d-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f633d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f633d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f633d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f633d-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f633d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f633d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f633d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f633d-124"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="f633d-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="f633d-125">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="f633d-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f633d-126">**DFM \_ GETHELPTEXT** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f633d-126">**DFM\_GETHELPTEXT** (ANSI)</span></span><br/>                                              |



 

 




