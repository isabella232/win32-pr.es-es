---
description: 'DFM_GETHELPTEXT mensaje: permite que el objeto de devolución de llamada especifique una cadena de texto de ayuda.'
title: DFM_GETHELPTEXT mensaje (Shlobj.h)
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
ms.openlocfilehash: 2428fe6696ff5949a0b25487437c8f3408b95f65
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097073"
---
# <a name="dfm_gethelptext-message"></a><span data-ttu-id="808be-103">Mensaje \_ GETHELPTEXT de DFM</span><span class="sxs-lookup"><span data-stu-id="808be-103">DFM\_GETHELPTEXT message</span></span>

<span data-ttu-id="808be-104">Permite que el objeto de devolución de llamada especifique una cadena de texto de ayuda.</span><span class="sxs-lookup"><span data-stu-id="808be-104">Allows the callback object to specify a help text string.</span></span>


```C++
DFM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="808be-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="808be-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="808be-106">*idCmd \_ cchMax* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="808be-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="808be-107">La palabra de orden bajo de este parámetro contiene el identificador del comando.</span><span class="sxs-lookup"><span data-stu-id="808be-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="808be-108">La palabra de orden superior contiene el número de caracteres del *búfer pszText.*</span><span class="sxs-lookup"><span data-stu-id="808be-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="808be-109">*pszText* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="808be-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="808be-110">Cadena ANSI terminada en NULL que contiene el texto de ayuda.</span><span class="sxs-lookup"><span data-stu-id="808be-110">A null-terminated ANSI string containing the help text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="808be-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="808be-111">Remarks</span></span>

<span data-ttu-id="808be-112">Este mensaje se envía a la función de devolución de llamada o al objeto de devolución de llamada en función de cómo se construya el objeto de menú contextual predeterminado.</span><span class="sxs-lookup"><span data-stu-id="808be-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="808be-113">Hay dos API para su construcción, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)y [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="808be-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="808be-114">[**DFM \_ INVOKECOMMANDEX es**](dfm-invokecommandex.md) una versión extendida de este mensaje y proporciona más información a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="808be-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="808be-115">Use **DFM \_ INVOKECOMMANDEX** si la información adicional proporcionada por esa interfaz es necesaria en la implementación.</span><span class="sxs-lookup"><span data-stu-id="808be-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="808be-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="808be-116">Requirements</span></span>



| <span data-ttu-id="808be-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="808be-117">Requirement</span></span> | <span data-ttu-id="808be-118">Valor</span><span class="sxs-lookup"><span data-stu-id="808be-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="808be-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="808be-119">Minimum supported client</span></span><br/> | <span data-ttu-id="808be-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="808be-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="808be-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="808be-121">Minimum supported server</span></span><br/> | <span data-ttu-id="808be-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="808be-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="808be-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="808be-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="808be-124"><dt>Shlobj.h</dt></span><span class="sxs-lookup"><span data-stu-id="808be-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="808be-125">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="808be-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="808be-126">**DFM \_ GETHELPTEXT** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="808be-126">**DFM\_GETHELPTEXT** (ANSI)</span></span><br/>                                              |



 

 




