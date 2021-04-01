---
title: Mensaje de MCIWNDM_GETEND (VFW. h)
description: El \_ mensaje MCIWNDM GETEND recupera la ubicación del final del contenido de un dispositivo MCI o un archivo. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetEnd.
ms.assetid: 3fa45928-af63-4f87-835d-f409011a797e
keywords:
- Mensaje de MCIWNDM_GETEND de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETEND
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d18057619e31fa9b22d7f6354527c394c02798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905570"
---
# <a name="mciwndm_getend-message"></a><span data-ttu-id="5a256-105">MCIWNDM \_ GETEND</span><span class="sxs-lookup"><span data-stu-id="5a256-105">MCIWNDM\_GETEND message</span></span>

<span data-ttu-id="5a256-106">El mensaje **MCIWNDM \_ GETEND** recupera la ubicación del final del contenido de un dispositivo MCI o un archivo.</span><span class="sxs-lookup"><span data-stu-id="5a256-106">The **MCIWNDM\_GETEND** message retrieves the location of the end of the content of an MCI device or file.</span></span> <span data-ttu-id="5a256-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) .</span><span class="sxs-lookup"><span data-stu-id="5a256-107">You can send this message explicitly or by using the [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) macro.</span></span>


```C++
MCIWNDM_GETEND 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="5a256-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5a256-108">Return Value</span></span>

<span data-ttu-id="5a256-109">Devuelve la ubicación en el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="5a256-109">Returns the location in the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a256-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a256-110">Requirements</span></span>



| <span data-ttu-id="5a256-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a256-111">Requirement</span></span> | <span data-ttu-id="5a256-112">Value</span><span class="sxs-lookup"><span data-stu-id="5a256-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5a256-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a256-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5a256-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5a256-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5a256-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a256-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5a256-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5a256-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5a256-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a256-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a256-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a256-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a256-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a256-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a256-120">**MCIWndGetEnd**</span><span class="sxs-lookup"><span data-stu-id="5a256-120">**MCIWndGetEnd**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
</dt> </dl>

 

 





