---
description: 'Permite que el objeto de devolución de llamada solicite la enumeración en un subproceso en segundo plano. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_BACKGROUNDENUM (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8428179c-2ec9-4979-9281-c2439e58beb6
api_name:
- SFVM_BACKGROUNDENUM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cb0b85abb3ca6830610a35502f55c0867a5ffbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997828"
---
# <a name="sfvm_backgroundenum-message"></a><span data-ttu-id="fd7ff-104">SFVM \_ BACKGROUNDENUM</span><span class="sxs-lookup"><span data-stu-id="fd7ff-104">SFVM\_BACKGROUNDENUM message</span></span>

<span data-ttu-id="fd7ff-105">Permite que el objeto de devolución de llamada solicite la enumeración en un subproceso en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-105">Allows the callback object to request enumeration on a background thread.</span></span> <span data-ttu-id="fd7ff-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="fd7ff-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++

                SFVM_BACKGROUNDENUM

            
```



## <a name="parameters"></a><span data-ttu-id="fd7ff-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd7ff-107">Parameters</span></span>

<span data-ttu-id="fd7ff-108">Este mensaje no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-108">This message has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd7ff-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd7ff-109">Remarks</span></span>

<span data-ttu-id="fd7ff-110">En respuesta a esta notificación, vuelva \_ a aceptar para habilitar la enumeración en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-110">In response to this notification, return S\_OK to enable background enumeration.</span></span> <span data-ttu-id="fd7ff-111">De forma predeterminada, el objeto de la carpeta del sistema mostrará la animación "linterna" mientras se está llevando a cabo la enumeración.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-111">By default, the system folder object will display the "flashlight" animation while the enumeration is taking place.</span></span> <span data-ttu-id="fd7ff-112">Para especificar una animación personalizada, controle [**SFVM \_ GETANIMATION**](sfvm-getanimation.md).</span><span class="sxs-lookup"><span data-stu-id="fd7ff-112">To specify a custom animation, handle [**SFVM\_GETANIMATION**](sfvm-getanimation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd7ff-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd7ff-113">Requirements</span></span>



| <span data-ttu-id="fd7ff-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd7ff-114">Requirement</span></span> | <span data-ttu-id="fd7ff-115">Value</span><span class="sxs-lookup"><span data-stu-id="fd7ff-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fd7ff-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd7ff-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fd7ff-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fd7ff-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fd7ff-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd7ff-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fd7ff-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fd7ff-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fd7ff-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd7ff-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd7ff-121"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd7ff-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
