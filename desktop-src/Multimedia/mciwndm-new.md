---
title: Mensaje de MCIWNDM_NEW (VFW. h)
description: El \_ nuevo mensaje MCIWNDM crea un nuevo archivo para el dispositivo MCI actual. Puede enviar este mensaje explícitamente o mediante la macro MCIWndNew.
ms.assetid: 18b2340d-8303-415a-867f-bd346034db2a
keywords:
- Mensaje de MCIWNDM_NEW de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293323cd0404da45e648024b35b7f96ef60fea61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802023"
---
# <a name="mciwndm_new-message"></a><span data-ttu-id="2fceb-105">MCIWNDM \_ nuevo mensaje</span><span class="sxs-lookup"><span data-stu-id="2fceb-105">MCIWNDM\_NEW message</span></span>

<span data-ttu-id="2fceb-106">El **\_ nuevo mensaje MCIWNDM** crea un nuevo archivo para el dispositivo MCI actual.</span><span class="sxs-lookup"><span data-stu-id="2fceb-106">The **MCIWNDM\_NEW** message creates a new file for the current MCI device.</span></span> <span data-ttu-id="2fceb-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) .</span><span class="sxs-lookup"><span data-stu-id="2fceb-107">You can send this message explicitly or by using the [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro.</span></span>


```C++
MCIWNDM_NEW 
wParam = 0; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="2fceb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2fceb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fceb-109"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="2fceb-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="2fceb-110">Puntero a un búfer que contiene el nombre del dispositivo MCI que utilizará el archivo.</span><span class="sxs-lookup"><span data-stu-id="2fceb-110">Pointer to a buffer containing the name of the MCI device that will use the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fceb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2fceb-111">Return Value</span></span>

<span data-ttu-id="2fceb-112">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2fceb-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fceb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fceb-113">Requirements</span></span>



| <span data-ttu-id="2fceb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fceb-114">Requirement</span></span> | <span data-ttu-id="2fceb-115">Value</span><span class="sxs-lookup"><span data-stu-id="2fceb-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2fceb-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fceb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2fceb-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2fceb-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2fceb-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fceb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2fceb-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2fceb-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2fceb-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2fceb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fceb-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fceb-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fceb-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fceb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fceb-123">**MCIWndNew**</span><span class="sxs-lookup"><span data-stu-id="2fceb-123">**MCIWndNew**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)
</dt> </dl>

 

 





