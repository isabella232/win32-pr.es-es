---
description: Se envía para comprobar la existencia de un comando de menú.
title: Mensaje de DFM_VALIDATECMD (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 97ff3cdf-ed0c-4813-8d5a-b5141636d32c
api_name:
- DFM_VALIDATECMD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5aa171f19d4d08c3ba3088676a4ae5364f0826f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153914"
---
# <a name="dfm_validatecmd-message"></a><span data-ttu-id="1ece3-103">DFM \_ VALIDATECMD</span><span class="sxs-lookup"><span data-stu-id="1ece3-103">DFM\_VALIDATECMD message</span></span>

<span data-ttu-id="1ece3-104">Se envía para comprobar la existencia de un comando de menú.</span><span class="sxs-lookup"><span data-stu-id="1ece3-104">Sent to verify the existence of a menu command.</span></span>


```C++
DFM_INVOKECOMMAND

    wParam = (WPARAM)(WPARAM) idCmd;            

    lParam = (LPARAM)(LPARAM) lParam = 0;

            
```



## <a name="parameters"></a><span data-ttu-id="1ece3-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ece3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ece3-106">*idCmd*</span><span class="sxs-lookup"><span data-stu-id="1ece3-106">*idCmd*</span></span> 
</dt> <dd><span data-ttu-id="1ece3-107">Desplazamiento del identificador del comando de menú.</span><span class="sxs-lookup"><span data-stu-id="1ece3-107">The menu command identifier offset.</span></span></dd> <dt>

<span data-ttu-id="1ece3-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ece3-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1ece3-109">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="1ece3-109">Not used.</span></span> <span data-ttu-id="1ece3-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1ece3-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ece3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ece3-111">Return value</span></span>

<span data-ttu-id="1ece3-112">Devuelve S \_ OK si el comando existe o S \_ false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1ece3-112">Returns S\_OK if the command exists, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ece3-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ece3-113">Remarks</span></span>

<span data-ttu-id="1ece3-114">Este mensaje se envía a la función de devolución de llamada o al objeto de devolución de llamada, dependiendo de cómo se construya el objeto de menú contextual predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1ece3-114">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="1ece3-115">Hay dos API para su construcción, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="1ece3-115">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="1ece3-116">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) es una versión extendida de este mensaje y proporciona más información a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="1ece3-116">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="1ece3-117">Use **DFM \_ INVOKECOMMANDEX** si necesita la información adicional proporcionada por esa interfaz en su implementación de.</span><span class="sxs-lookup"><span data-stu-id="1ece3-117">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ece3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ece3-118">Requirements</span></span>



| <span data-ttu-id="1ece3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ece3-119">Requirement</span></span> | <span data-ttu-id="1ece3-120">Value</span><span class="sxs-lookup"><span data-stu-id="1ece3-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1ece3-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ece3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1ece3-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1ece3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1ece3-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ece3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1ece3-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ece3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1ece3-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ece3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ece3-126"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ece3-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




