---
description: 'Permite que el objeto de devolución de llamada proporcione información de zona de Internet. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: 6fae7925-b1be-4270-9318-7fa517563dad
title: Mensaje de SFVM_GETZONE (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5586188aeab6a054e22e4b242039beaae1ce390d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546934"
---
# <a name="sfvm_getzone-message"></a><span data-ttu-id="da5c0-104">SFVM \_ GETZONE</span><span class="sxs-lookup"><span data-stu-id="da5c0-104">SFVM\_GETZONE message</span></span>

<span data-ttu-id="da5c0-105">\[Esta notificación se admite a través de Windows XP Service Pack 2 (SP2) y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="da5c0-105">\[This notification is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="da5c0-106">Es posible que no se admita en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="da5c0-106">It might be unsupported in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="da5c0-107">Permite que el objeto de devolución de llamada proporcione información de zona de Internet.</span><span class="sxs-lookup"><span data-stu-id="da5c0-107">Allows the callback object to provide Internet zone information.</span></span> <span data-ttu-id="da5c0-108">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="da5c0-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETZONE
    lParam = (LPARAM)(DWORD*) zone;
            
```



## <a name="parameters"></a><span data-ttu-id="da5c0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da5c0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da5c0-110">*zona* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="da5c0-110">*zone* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da5c0-111">Uno de los siguientes valores que indican la zona de Internet.</span><span class="sxs-lookup"><span data-stu-id="da5c0-111">One of the following values indicating the Internet zone.</span></span> <span data-ttu-id="da5c0-112">Estos valores constituyen la enumeración [**URLZONE**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) , que se define en urlmon. h.</span><span class="sxs-lookup"><span data-stu-id="da5c0-112">These values constitute the [**URLZONE**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) enumeration, defined in Urlmon.h.</span></span>

<dt>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>

<span data-ttu-id="da5c0-113"><span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**\_máquina local \_ URLZONE**</span><span class="sxs-lookup"><span data-stu-id="da5c0-113"><span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**URLZONE\_LOCAL\_MACHINE**</span></span>


</dt> <dd>

<span data-ttu-id="da5c0-114">Zona utilizada para el contenido que ya está en el equipo local del usuario.</span><span class="sxs-lookup"><span data-stu-id="da5c0-114">Zone used for content already on the user's local computer.</span></span> <span data-ttu-id="da5c0-115">La interfaz de usuario no expone esta zona.</span><span class="sxs-lookup"><span data-stu-id="da5c0-115">This zone is not exposed by the user interface.</span></span>

</dd> <dt>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>

<span data-ttu-id="da5c0-116"><span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**Intranet de URLZONE \_**</span><span class="sxs-lookup"><span data-stu-id="da5c0-116"><span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**URLZONE\_INTRANET**</span></span>


</dt> <dd>

<span data-ttu-id="da5c0-117">Zona utilizada para el contenido que se encuentra en una intranet.</span><span class="sxs-lookup"><span data-stu-id="da5c0-117">Zone used for content found on an intranet.</span></span>

</dd> <dt>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>

<span data-ttu-id="da5c0-118"><span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**URLZONE de \_ confianza**</span><span class="sxs-lookup"><span data-stu-id="da5c0-118"><span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**URLZONE\_TRUSTED**</span></span>


</dt> <dd>

<span data-ttu-id="da5c0-119">Zona utilizada para sitios web de confianza en Internet.</span><span class="sxs-lookup"><span data-stu-id="da5c0-119">Zone used for trusted websites on the Internet.</span></span>

</dd> <dt>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>

<span data-ttu-id="da5c0-120"><span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**URLZONE \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="da5c0-120"><span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**URLZONE\_INTERNET**</span></span>


</dt> <dd>

<span data-ttu-id="da5c0-121">Zona utilizada para la mayor parte del contenido de Internet.</span><span class="sxs-lookup"><span data-stu-id="da5c0-121">Zone used for most of the content on the Internet.</span></span>

</dd> <dt>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>

<span data-ttu-id="da5c0-122"><span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**URLZONE que no es de \_ confianza**</span><span class="sxs-lookup"><span data-stu-id="da5c0-122"><span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**URLZONE\_UNTRUSTED**</span></span>


</dt> <dd>

<span data-ttu-id="da5c0-123">Zona usada para sitios web que no son de confianza.</span><span class="sxs-lookup"><span data-stu-id="da5c0-123">Zone used for websites that are not trusted.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da5c0-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da5c0-124">Requirements</span></span>



| <span data-ttu-id="da5c0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="da5c0-125">Requirement</span></span> | <span data-ttu-id="da5c0-126">Value</span><span class="sxs-lookup"><span data-stu-id="da5c0-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="da5c0-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da5c0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="da5c0-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="da5c0-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="da5c0-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da5c0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="da5c0-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="da5c0-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="da5c0-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da5c0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="da5c0-132"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="da5c0-132"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
