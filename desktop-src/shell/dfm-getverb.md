---
description: Enviado por la implementación predeterminada del menú contextual para obtener el verbo para el identificador de comando especificado en el menú contextual.
title: Mensaje de DFM_GETVERB (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bd12a38e-4d50-43ad-9d1f-8fefa90b44f9
api_name:
- DFM_GETVERB
- DFM_GETVERBA
- DFM_GETVERBW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bbb1b2fb54aa2b0e4b66cf8fc559c56eb279504d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275236"
---
# <a name="dfm_getverb-message"></a><span data-ttu-id="c7be4-103">DFM \_ GETVERB</span><span class="sxs-lookup"><span data-stu-id="c7be4-103">DFM\_GETVERB message</span></span>

<span data-ttu-id="c7be4-104">Enviado por la implementación predeterminada del menú contextual para obtener el verbo para el identificador de comando especificado en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="c7be4-104">Sent by the default context menu implementation to get the verb for the given command ID in the context menu.</span></span>


```C++

                DFM_GETVERB 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="c7be4-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7be4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7be4-106">*idCmd \_ cchMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="c7be4-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7be4-107">La palabra de orden inferior de este parámetro contiene el identificador de comando.</span><span class="sxs-lookup"><span data-stu-id="c7be4-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="c7be4-108">La palabra de orden superior contiene el número de caracteres en el búfer de *miembros pszText* .</span><span class="sxs-lookup"><span data-stu-id="c7be4-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c7be4-109">*miembros pszText* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c7be4-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7be4-110">Puntero a una cadena terminada en null que contiene el texto del verbo.</span><span class="sxs-lookup"><span data-stu-id="c7be4-110">A pointer to a null-terminated string that contains the verb text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7be4-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7be4-111">Remarks</span></span>

<span data-ttu-id="c7be4-112">Este mensaje se envía a la función de devolución de llamada o al objeto de devolución de llamada, dependiendo de cómo se construya el objeto de menú contextual predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c7be4-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="c7be4-113">Hay dos API para su construcción, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="c7be4-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="c7be4-114">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) es una versión extendida de este mensaje y proporciona más información a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="c7be4-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="c7be4-115">Use **DFM \_ INVOKECOMMANDEX** si necesita la información adicional proporcionada por esa interfaz en su implementación de.</span><span class="sxs-lookup"><span data-stu-id="c7be4-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7be4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7be4-116">Requirements</span></span>



| <span data-ttu-id="c7be4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7be4-117">Requirement</span></span> | <span data-ttu-id="c7be4-118">Value</span><span class="sxs-lookup"><span data-stu-id="c7be4-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c7be4-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7be4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c7be4-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c7be4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c7be4-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7be4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c7be4-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c7be4-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c7be4-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7be4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7be4-124"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7be4-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="c7be4-125">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="c7be4-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c7be4-126">**DFM \_ GETVERBW** (Unicode) y **DFM \_ GETVERBA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c7be4-126">**DFM\_GETVERBW** (Unicode) and **DFM\_GETVERBA** (ANSI)</span></span><br/>                 |



 

 




