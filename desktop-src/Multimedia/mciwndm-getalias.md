---
title: Mensaje de MCIWNDM_GETALIAS (VFW. h)
description: El \_ mensaje MCIWNDM GETALIAS recupera el alias usado para abrir un dispositivo MCI o un archivo con la función mciSendString. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetAlias.
ms.assetid: 37131b89-275c-4ab6-9278-0e08c42471bd
keywords:
- Mensaje de MCIWNDM_GETALIAS de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETALIAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e971c50b9abc450387ac29f9a7331bfdca5c38c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676592"
---
# <a name="mciwndm_getalias-message"></a><span data-ttu-id="9d0d4-105">MCIWNDM \_ GETALIAS</span><span class="sxs-lookup"><span data-stu-id="9d0d4-105">MCIWNDM\_GETALIAS message</span></span>

<span data-ttu-id="9d0d4-106">El mensaje **MCIWNDM \_ GETALIAS** recupera el alias usado para abrir un dispositivo MCI o un archivo con la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9d0d4-106">The **MCIWNDM\_GETALIAS** message retrieves the alias used to open an MCI device or file with the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="9d0d4-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) .</span><span class="sxs-lookup"><span data-stu-id="9d0d4-107">You can send this message explicitly or by using the [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) macro.</span></span>


```C++
MCIWNDM_GETALIAS 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="9d0d4-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d0d4-108">Return Value</span></span>

<span data-ttu-id="9d0d4-109">Devuelve el alias del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9d0d4-109">Returns the device alias.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d0d4-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d0d4-110">Requirements</span></span>



| <span data-ttu-id="9d0d4-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d0d4-111">Requirement</span></span> | <span data-ttu-id="9d0d4-112">Value</span><span class="sxs-lookup"><span data-stu-id="9d0d4-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9d0d4-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d0d4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9d0d4-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9d0d4-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9d0d4-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d0d4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9d0d4-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9d0d4-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9d0d4-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d0d4-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d0d4-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d0d4-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d0d4-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d0d4-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="9d0d4-120">[**mciSendString**](/previous-versions//dd757161(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9d0d4-120">[**mciSendString**](/previous-versions//dd757161(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9d0d4-121">**MCIWndGetAlias**</span><span class="sxs-lookup"><span data-stu-id="9d0d4-121">**MCIWndGetAlias**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias)
</dt> </dl>

 

