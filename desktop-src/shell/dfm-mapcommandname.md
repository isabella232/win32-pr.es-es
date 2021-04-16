---
description: Enviado por la implementación predeterminada del menú contextual para asignar un nombre a un comando de menú.
title: Mensaje de DFM_MAPCOMMANDNAME (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8aa764f7-d5d4-4a84-94d2-993265e1eb5a
api_name:
- DFM_MAPCOMMANDNAME
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 312817e5c530078b906af63e4e8c3d00595d3a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540502"
---
# <a name="dfm_mapcommandname-message"></a><span data-ttu-id="8836b-103">DFM \_ MAPCOMMANDNAME</span><span class="sxs-lookup"><span data-stu-id="8836b-103">DFM\_MAPCOMMANDNAME message</span></span>

<span data-ttu-id="8836b-104">Enviado por la implementación predeterminada del menú contextual para asignar un nombre a un comando de menú.</span><span class="sxs-lookup"><span data-stu-id="8836b-104">Sent by the default context menu implementation to assign a name to a menu command.</span></span>


```C++
DFM_MAPCOMMANDNAME

    lParam = (LPARAM)(int*) defaultID;

    wparam = (WPARAM)(LPTSTR) pszCommandName;

            
```



## <a name="parameters"></a><span data-ttu-id="8836b-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8836b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8836b-106">*defaultID* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8836b-106">*defaultID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8836b-107">Puntero al identificador del comando de menú seleccionado.</span><span class="sxs-lookup"><span data-stu-id="8836b-107">A pointer to the ID of the selected menu command.</span></span>

</dd> <dt>

<span data-ttu-id="8836b-108">*pszCommandName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8836b-108">*pszCommandName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8836b-109">Puntero a una cadena Unicode que contiene el nombre del comando.</span><span class="sxs-lookup"><span data-stu-id="8836b-109">A pointer to a Unicode string containing the name of the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8836b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8836b-110">Remarks</span></span>

<span data-ttu-id="8836b-111">Este mensaje se envía a la función de devolución de llamada o al objeto de devolución de llamada, dependiendo de cómo se implemente el objeto de menú contextual predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8836b-111">This message is sent to either the callback function or the callback object depending on how the default context menu object is implemented.</span></span> <span data-ttu-id="8836b-112">Hay dos API para su implementación, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="8836b-112">There are two APIs for its implementation, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="8836b-113">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) es una versión extendida de este mensaje y proporciona más información a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8836b-113">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="8836b-114">Use **DFM \_ INVOKECOMMANDEX** si necesita la información adicional proporcionada por esa interfaz en su implementación de.</span><span class="sxs-lookup"><span data-stu-id="8836b-114">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="8836b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8836b-115">Requirements</span></span>



| <span data-ttu-id="8836b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8836b-116">Requirement</span></span> | <span data-ttu-id="8836b-117">Value</span><span class="sxs-lookup"><span data-stu-id="8836b-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8836b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8836b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8836b-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8836b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8836b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8836b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8836b-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8836b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8836b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8836b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8836b-123"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="8836b-123"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




