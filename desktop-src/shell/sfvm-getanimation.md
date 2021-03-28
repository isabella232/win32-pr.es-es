---
description: 'Permite que el objeto de devolución de llamada especifique que se muestre una animación mientras los elementos se enumeran en un subproceso en segundo plano. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: 6f8b3894-f08f-4ebf-a645-87869e7d1b20
title: Mensaje de SFVM_GETANIMATION (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e4281689556e8315da7a9550fd69acc1a327a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156796"
---
# <a name="sfvm_getanimation-message"></a><span data-ttu-id="72bc0-104">SFVM \_ GETANIMATION</span><span class="sxs-lookup"><span data-stu-id="72bc0-104">SFVM\_GETANIMATION message</span></span>

<span data-ttu-id="72bc0-105">Permite que el objeto de devolución de llamada especifique que se muestre una animación mientras los elementos se enumeran en un subproceso en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="72bc0-105">Allows the callback object to specify that an animation be displayed while items are enumerated on a background thread.</span></span> <span data-ttu-id="72bc0-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="72bc0-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETANIMATION 

    wParam = (WPARAM)(HINSTANCE*) phinst;

    lParam = (LPARAM)(WCHAR*) pwszName;

            
```



## <a name="parameters"></a><span data-ttu-id="72bc0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72bc0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72bc0-108">*phinst* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="72bc0-108">*phinst* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72bc0-109">Identificador de instancia del módulo del que se debe cargar el recurso.</span><span class="sxs-lookup"><span data-stu-id="72bc0-109">The instance handle of the module that the resource should be loaded from.</span></span>

</dd> <dt>

<span data-ttu-id="72bc0-110">*pwszName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="72bc0-110">*pwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72bc0-111">Puntero a una cadena Unicode terminada en null que contiene la ruta de acceso del archivo. avi o el nombre de un recurso AVI.</span><span class="sxs-lookup"><span data-stu-id="72bc0-111">A pointer to a null-terminated Unicode string containing the path of the .avi file or the name of an AVI resource.</span></span> <span data-ttu-id="72bc0-112">Como alternativa, este parámetro puede constar del identificador de recurso en la palabra de orden inferior y de 0 en la palabra de orden superior.</span><span class="sxs-lookup"><span data-stu-id="72bc0-112">Alternatively, this parameter can consist of the resource identifier in the low-order word and 0 in the high-order word.</span></span> <span data-ttu-id="72bc0-113">Para crear este valor, use la macro [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) .</span><span class="sxs-lookup"><span data-stu-id="72bc0-113">To create this value, use the [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="72bc0-114">El control carga el recurso desde el módulo especificado por HINST.</span><span class="sxs-lookup"><span data-stu-id="72bc0-114">The control loads the resource from the module specified by hinst.</span></span> <span data-ttu-id="72bc0-115">Un recurso AVI debe tener el tipo "AVI".</span><span class="sxs-lookup"><span data-stu-id="72bc0-115">An AVI resource must have the "AVI" type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72bc0-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72bc0-116">Remarks</span></span>

<span data-ttu-id="72bc0-117">De forma predeterminada, el objeto de vista de carpeta del sistema muestra la animación de "linterna" durante una enumeración en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="72bc0-117">By default, the system folder view object displays the "flashlight" animation during a background enumeration.</span></span>

<span data-ttu-id="72bc0-118">*phinst* y *pwszName* se pasarán al [control Animation](../controls/animation-control-overview.md) con un mensaje [**\_ abierto ACM**](../controls/acm-open.md) .</span><span class="sxs-lookup"><span data-stu-id="72bc0-118">*phinst* and *pwszName* will be passed to the [animation control](../controls/animation-control-overview.md) with an [**ACM\_OPEN**](../controls/acm-open.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="72bc0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72bc0-119">Requirements</span></span>



| <span data-ttu-id="72bc0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="72bc0-120">Requirement</span></span> | <span data-ttu-id="72bc0-121">Value</span><span class="sxs-lookup"><span data-stu-id="72bc0-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="72bc0-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72bc0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="72bc0-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="72bc0-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="72bc0-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72bc0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="72bc0-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="72bc0-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="72bc0-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72bc0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="72bc0-127"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="72bc0-127"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
