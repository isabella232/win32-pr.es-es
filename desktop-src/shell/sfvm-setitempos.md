---
description: Establece la posición de un elemento en la vista de Shell. Usado por el \_ mensaje de SHShellFolderView.
title: Mensaje de SFVM_SETITEMPOS (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b89f2d62-095b-4cad-a47e-2d41e122cb3e
api_name:
- SFVM_SETITEMPOS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 450aeabee6e5edeba466e4a5fe64725c13eea32b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279188"
---
# <a name="sfvm_setitempos-message"></a><span data-ttu-id="7c0f6-104">SFVM \_ SETITEMPOS</span><span class="sxs-lookup"><span data-stu-id="7c0f6-104">SFVM\_SETITEMPOS message</span></span>

<span data-ttu-id="7c0f6-105">Establece la posición de un elemento en la vista de Shell.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-105">Sets the position of an item in the Shell view.</span></span> <span data-ttu-id="7c0f6-106">Usado por [**el \_ mensaje de SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="7c0f6-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++

                SFVM_SETITEMPOS 

    lParam = (LPSFV_SETITEMPOS)&sip;

            
```



## <a name="parameters"></a><span data-ttu-id="7c0f6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c0f6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c0f6-108">*SIP* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="7c0f6-108">*sip* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c0f6-109">Puntero a una estructura [**de \_ SETITEMPOS de SFV**](/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos) .</span><span class="sxs-lookup"><span data-stu-id="7c0f6-109">A pointer to an [**SFV\_SETITEMPOS**](/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c0f6-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c0f6-110">Requirements</span></span>



| <span data-ttu-id="7c0f6-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c0f6-111">Requirement</span></span> | <span data-ttu-id="7c0f6-112">Value</span><span class="sxs-lookup"><span data-stu-id="7c0f6-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7c0f6-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c0f6-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7c0f6-114">Solo aplicaciones de escritorio de Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="7c0f6-114">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7c0f6-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c0f6-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7c0f6-116">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7c0f6-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7c0f6-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c0f6-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c0f6-118"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c0f6-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




