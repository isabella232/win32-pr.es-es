---
description: 'Permite que el objeto de devolución de llamada especifique un archivo de ayuda HTML y un tema dentro de él. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_GETHELPTOPIC (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bbe92e9f-4074-4101-a945-072866ab20a8
api_name:
- SFVM_GETHELPTOPIC
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7ebe078934f467407710f0ad493b6088b34d0c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911397"
---
# <a name="sfvm_gethelptopic-message"></a><span data-ttu-id="a8263-104">SFVM \_ GETHELPTOPIC</span><span class="sxs-lookup"><span data-stu-id="a8263-104">SFVM\_GETHELPTOPIC message</span></span>

<span data-ttu-id="a8263-105">Permite que el objeto de devolución de llamada especifique un archivo de ayuda HTML y un tema dentro de él.</span><span class="sxs-lookup"><span data-stu-id="a8263-105">Allows the callback object to specify an HTML Help file and a topic within it.</span></span> <span data-ttu-id="a8263-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="a8263-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETHELPTOPIC 

    lParam = (LPARAM)(SFVM_HELPTOPIC_DATA*) phtd;

            
```



## <a name="parameters"></a><span data-ttu-id="a8263-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8263-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8263-108">*phtd* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a8263-108">*phtd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8263-109">Dirección de una estructura [**de \_ \_ datos de SFVM HELPTOPIC**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data) que especifica el archivo de ayuda HTML y el tema.</span><span class="sxs-lookup"><span data-stu-id="a8263-109">The address of a [**SFVM\_HELPTOPIC\_DATA**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data) structure that specifies the HTML Help file and topic.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8263-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8263-110">Requirements</span></span>



| <span data-ttu-id="a8263-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8263-111">Requirement</span></span> | <span data-ttu-id="a8263-112">Value</span><span class="sxs-lookup"><span data-stu-id="a8263-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a8263-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8263-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a8263-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a8263-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a8263-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8263-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a8263-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a8263-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a8263-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8263-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8263-118"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8263-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
