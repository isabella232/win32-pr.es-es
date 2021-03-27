---
description: SFVM \_ GETPANE puede modificarse o no estar disponible.
ms.assetid: 9621b921-e97f-4219-953a-7c961a81c379
title: Mensaje de SFVM_GETPANE (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2800be1b7b427e13014686e587b51fc4bf7d7617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002300"
---
# <a name="sfvm_getpane-message"></a><span data-ttu-id="4b4cb-103">SFVM \_ GETPANE</span><span class="sxs-lookup"><span data-stu-id="4b4cb-103">SFVM\_GETPANE message</span></span>

<span data-ttu-id="4b4cb-104">\[**SFVM \_ GETPANE** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="4b4cb-104">\[**SFVM\_GETPANE** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4b4cb-105">En versiones posteriores podría modificarse o no estar disponible.\]</span><span class="sxs-lookup"><span data-stu-id="4b4cb-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="4b4cb-106">Permite que el objeto de devolución de llamada proporcione el panel de la barra de estado en el que se va a mostrar la información de la zona de Internet.</span><span class="sxs-lookup"><span data-stu-id="4b4cb-106">Allows the callback object to provide the status bar pane in which to display the Internet zone information.</span></span> <span data-ttu-id="4b4cb-107">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="4b4cb-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETPANE
    wParam = (WPARAM)(int) paneID;
    lParam = (LPARAM)(DWORD*) pane;
            
```



## <a name="parameters"></a><span data-ttu-id="4b4cb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b4cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b4cb-109">*paneID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b4cb-109">*paneID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b4cb-110">IDENTIFICADOR del panel solicitado.</span><span class="sxs-lookup"><span data-stu-id="4b4cb-110">ID of the requested pane.</span></span> <span data-ttu-id="4b4cb-111">Suele \_ ser la zona del panel, pero puede ser cualquiera de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4b4cb-111">This is normally PANE\_ZONE, but can be any one of the following values.</span></span>

<dt>

<span id="PANE_NONE"></span><span id="pane_none"></span>

<span data-ttu-id="4b4cb-112"><span id="PANE_NONE"></span><span id="pane_none"></span>**ninguno de los paneles \_**</span><span class="sxs-lookup"><span data-stu-id="4b4cb-112"><span id="PANE_NONE"></span><span id="pane_none"></span>**PANE\_NONE**</span></span>


</dt> <dd>

<span data-ttu-id="4b4cb-113">Ningún panel.</span><span class="sxs-lookup"><span data-stu-id="4b4cb-113">No pane.</span></span>

</dd> <dt>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>

<span data-ttu-id="4b4cb-114"><span id="PANE_ZONE"></span><span id="pane_zone"></span>**zona del panel \_**</span><span class="sxs-lookup"><span data-stu-id="4b4cb-114"><span id="PANE_ZONE"></span><span id="pane_zone"></span>**PANE\_ZONE**</span></span>


</dt> <dd>

<span data-ttu-id="4b4cb-115">Panel zona de Internet.</span><span class="sxs-lookup"><span data-stu-id="4b4cb-115">The Internet zone pane.</span></span>

</dd> <dt>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>

<span data-ttu-id="4b4cb-116"><span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**PANEL \_ sin conexión**</span><span class="sxs-lookup"><span data-stu-id="4b4cb-116"><span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**PANE\_OFFLINE**</span></span>


</dt> <dd>

<span data-ttu-id="4b4cb-117">Panel sin conexión.</span><span class="sxs-lookup"><span data-stu-id="4b4cb-117">The offline pane.</span></span>

</dd> <dt>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>

<span data-ttu-id="4b4cb-118"><span id="PANE_PRINTER"></span><span id="pane_printer"></span>**impresora de panel \_**</span><span class="sxs-lookup"><span data-stu-id="4b4cb-118"><span id="PANE_PRINTER"></span><span id="pane_printer"></span>**PANE\_PRINTER**</span></span>


</dt> <dd>

<span data-ttu-id="4b4cb-119">El panel de indicación de impresión.</span><span class="sxs-lookup"><span data-stu-id="4b4cb-119">The print indication pane.</span></span>

</dd> <dt>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>

<span data-ttu-id="4b4cb-120"><span id="PANE_SSL"></span><span id="pane_ssl"></span>**SSL de panel \_**</span><span class="sxs-lookup"><span data-stu-id="4b4cb-120"><span id="PANE_SSL"></span><span id="pane_ssl"></span>**PANE\_SSL**</span></span>


</dt> <dd>

<span data-ttu-id="4b4cb-121">El panel SSL.</span><span class="sxs-lookup"><span data-stu-id="4b4cb-121">The SSL pane.</span></span>

</dd> <dt>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>

<span data-ttu-id="4b4cb-122"><span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**navegación de panel \_**</span><span class="sxs-lookup"><span data-stu-id="4b4cb-122"><span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**PANE\_NAVIGATION**</span></span>


</dt> <dd>

<span data-ttu-id="4b4cb-123">Panel de navegación.</span><span class="sxs-lookup"><span data-stu-id="4b4cb-123">The navigation pane.</span></span>

</dd> <dt>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>

<span data-ttu-id="4b4cb-124"><span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**progreso del panel \_**</span><span class="sxs-lookup"><span data-stu-id="4b4cb-124"><span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**PANE\_PROGRESS**</span></span>


</dt> <dd>

<span data-ttu-id="4b4cb-125">Panel de la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="4b4cb-125">The progress bar pane.</span></span>

</dd> <dt>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>

<span data-ttu-id="4b4cb-126"><span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**privacidad del panel \_**</span><span class="sxs-lookup"><span data-stu-id="4b4cb-126"><span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**PANE\_PRIVACY**</span></span>


</dt> <dd>

<span data-ttu-id="4b4cb-127">El panel indicador de privacidad.</span><span class="sxs-lookup"><span data-stu-id="4b4cb-127">The privacy indicator pane.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4b4cb-128">*Panel* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4b4cb-128">*pane* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b4cb-129">Puntero a un **valor DWORD** que contiene el número del panel.</span><span class="sxs-lookup"><span data-stu-id="4b4cb-129">Pointer to a **DWORD** containing the pane number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4b4cb-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b4cb-130">Requirements</span></span>



| <span data-ttu-id="4b4cb-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b4cb-131">Requirement</span></span> | <span data-ttu-id="4b4cb-132">Value</span><span class="sxs-lookup"><span data-stu-id="4b4cb-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4b4cb-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b4cb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4b4cb-134">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4b4cb-134">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4b4cb-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b4cb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4b4cb-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4b4cb-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4b4cb-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="4b4cb-137">End of client support</span></span><br/>    | <span data-ttu-id="4b4cb-138">Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="4b4cb-138">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="4b4cb-139">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="4b4cb-139">End of server support</span></span><br/>    | <span data-ttu-id="4b4cb-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4b4cb-140">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="4b4cb-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b4cb-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b4cb-142"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b4cb-142"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
