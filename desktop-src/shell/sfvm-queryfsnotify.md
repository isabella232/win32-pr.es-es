---
description: SFVM \_ QUERYFSNOTIFY puede modificarse o no estar disponible.
ms.assetid: 5d777115-bae3-47c4-9edc-c99c40a4f926
title: Mensaje de SFVM_QUERYFSNOTIFY (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4416bda249e3ec0f2a0c0f2d45ac353961e180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279392"
---
# <a name="sfvm_queryfsnotify-message"></a><span data-ttu-id="bd88a-103">SFVM \_ QUERYFSNOTIFY</span><span class="sxs-lookup"><span data-stu-id="bd88a-103">SFVM\_QUERYFSNOTIFY message</span></span>

<span data-ttu-id="bd88a-104">\[**SFVM \_ QUERYFSNOTIFY** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="bd88a-104">\[**SFVM\_QUERYFSNOTIFY** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bd88a-105">En versiones posteriores podría modificarse o no estar disponible.\]</span><span class="sxs-lookup"><span data-stu-id="bd88a-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="bd88a-106">Permite que el objeto de devolución de llamada registre una carpeta para que los cambios en la vista de esa carpeta generen notificaciones.</span><span class="sxs-lookup"><span data-stu-id="bd88a-106">Allows the callback object to register a folder so that changes to that folder's view will generate notifications.</span></span> <span data-ttu-id="bd88a-107">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="bd88a-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_QUERYFSNOTIFY 
    lParam = (LPARAM)(SHChangeNotifyEntry*) shcne;
            
```



## <a name="parameters"></a><span data-ttu-id="bd88a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd88a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd88a-109">*shcne* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bd88a-109">*shcne* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd88a-110">Estructura que contiene el PIDL del elemento que se va a inspeccionar en busca de eventos y una indicación de si también se deben inspeccionar las subcarpetas de ese elemento.</span><span class="sxs-lookup"><span data-stu-id="bd88a-110">A structure to hold the PIDL of the item to watch for events and an indication whether subfolders of that item should also be watched.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bd88a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd88a-111">Requirements</span></span>



| <span data-ttu-id="bd88a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd88a-112">Requirement</span></span> | <span data-ttu-id="bd88a-113">Value</span><span class="sxs-lookup"><span data-stu-id="bd88a-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bd88a-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd88a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="bd88a-115">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="bd88a-115">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bd88a-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd88a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="bd88a-117">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bd88a-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bd88a-118">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="bd88a-118">End of client support</span></span><br/>    | <span data-ttu-id="bd88a-119">Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="bd88a-119">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="bd88a-120">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="bd88a-120">End of server support</span></span><br/>    | <span data-ttu-id="bd88a-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bd88a-121">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="bd88a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd88a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd88a-123"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd88a-123"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
