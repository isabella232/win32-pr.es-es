---
title: Mensaje de MCIWNDM_GETLENGTH (VFW. h)
description: El mensaje de MCIWNDM \_ GETLENGTH recupera la longitud del contenido o del archivo que usa actualmente un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetLength.
ms.assetid: bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f
keywords:
- Mensaje de MCIWNDM_GETLENGTH de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETLENGTH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2347647fcff0beb87be12b7f6a05790b97f36d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489419"
---
# <a name="mciwndm_getlength-message"></a><span data-ttu-id="ae728-105">Mensaje de MCIWNDM \_ GETLENGTH</span><span class="sxs-lookup"><span data-stu-id="ae728-105">MCIWNDM\_GETLENGTH message</span></span>

<span data-ttu-id="ae728-106">El mensaje de **MCIWNDM \_ GETLENGTH** recupera la longitud del contenido o del archivo que usa actualmente un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="ae728-106">The **MCIWNDM\_GETLENGTH** message retrieves the length of the content or file currently used by an MCI device.</span></span> <span data-ttu-id="ae728-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) .</span><span class="sxs-lookup"><span data-stu-id="ae728-107">You can send this message explicitly or by using the [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) macro.</span></span>


```C++
MCIWNDM_GETLENGTH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="ae728-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae728-108">Return Value</span></span>

<span data-ttu-id="ae728-109">Devuelve la longitud.</span><span class="sxs-lookup"><span data-stu-id="ae728-109">Returns the length.</span></span> <span data-ttu-id="ae728-110">Las unidades de la longitud dependen del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="ae728-110">The units for the length depend on the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae728-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae728-111">Requirements</span></span>



| <span data-ttu-id="ae728-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae728-112">Requirement</span></span> | <span data-ttu-id="ae728-113">Value</span><span class="sxs-lookup"><span data-stu-id="ae728-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ae728-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae728-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ae728-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ae728-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ae728-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae728-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ae728-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ae728-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ae728-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae728-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae728-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae728-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae728-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae728-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae728-121">**MCIWndGetLength**</span><span class="sxs-lookup"><span data-stu-id="ae728-121">**MCIWndGetLength**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
</dt> </dl>

 

 





