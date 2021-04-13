---
description: SFVM \_ GETDETAILSOF puede modificarse o no estar disponible.
ms.assetid: 46a81a7b-527c-4d41-8d25-ce65fd87416e
title: Mensaje de SFVM_GETDETAILSOF (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6170c0fc8dc29435b2c6f2bb033f30706ccb7b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985770"
---
# <a name="sfvm_getdetailsof-message"></a><span data-ttu-id="56c90-103">SFVM \_ GETDETAILSOF</span><span class="sxs-lookup"><span data-stu-id="56c90-103">SFVM\_GETDETAILSOF message</span></span>

<span data-ttu-id="56c90-104">\[**SFVM \_ GETDETAILSOF** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="56c90-104">\[**SFVM\_GETDETAILSOF** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="56c90-105">En versiones posteriores podría modificarse o no estar disponible.\]</span><span class="sxs-lookup"><span data-stu-id="56c90-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="56c90-106">Permite que el objeto de devolución de llamada proporcione los detalles de un elemento en una carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="56c90-106">Allows the callback object to provide the details for an item in a Shell folder.</span></span> <span data-ttu-id="56c90-107">Use solo si se produce un error en una llamada a [**IShellFolder2:: GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) y no hay ningún método [**IShellDetails:: GetDetailsOf**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) disponible para llamar a.</span><span class="sxs-lookup"><span data-stu-id="56c90-107">Use only if a call to [**IShellFolder2::GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) fails and there is no [**IShellDetails::GetDetailsOf**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) method available to call.</span></span> <span data-ttu-id="56c90-108">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="56c90-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETDETAILSOF
    wParam = (WPARAM)(int) iColumn;
    lParam = (LPARAM)(DETAILSINFO*) pDi;
            
```



## <a name="parameters"></a><span data-ttu-id="56c90-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56c90-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56c90-110">*iColumn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="56c90-110">*iColumn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56c90-111">IDENTIFICADOR de base cero de la columna.</span><span class="sxs-lookup"><span data-stu-id="56c90-111">The zero-based ID of the column.</span></span>

</dd> <dt>

<span data-ttu-id="56c90-112">*pDi* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="56c90-112">*pDi* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56c90-113">Puntero a una estructura [**DETAILSINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo) rellena con la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="56c90-113">A pointer to a [**DETAILSINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo) structure filled with the requested information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56c90-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56c90-114">Requirements</span></span>



| <span data-ttu-id="56c90-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="56c90-115">Requirement</span></span> | <span data-ttu-id="56c90-116">Value</span><span class="sxs-lookup"><span data-stu-id="56c90-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="56c90-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56c90-117">Minimum supported client</span></span><br/> | <span data-ttu-id="56c90-118">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="56c90-118">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="56c90-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56c90-119">Minimum supported server</span></span><br/> | <span data-ttu-id="56c90-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="56c90-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="56c90-121">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="56c90-121">End of client support</span></span><br/>    | <span data-ttu-id="56c90-122">Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="56c90-122">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="56c90-123">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="56c90-123">End of server support</span></span><br/>    | <span data-ttu-id="56c90-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="56c90-124">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="56c90-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56c90-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="56c90-126"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="56c90-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
