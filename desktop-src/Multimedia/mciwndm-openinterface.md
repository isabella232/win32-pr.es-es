---
title: Mensaje de MCIWNDM_OPENINTERFACE (VFW. h)
description: El \_ mensaje OPENINTERFACE de MCIWNDM asocia el flujo de datos o el archivo asociado a la interfaz especificada a una ventana de MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro MCIWndOpenInterface.
ms.assetid: 73cbd637-d315-4b39-a978-2b72aed1f303
keywords:
- Mensaje de MCIWNDM_OPENINTERFACE de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_OPENINTERFACE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c40453f4d587429508a5aae19bc432fc46088ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421908"
---
# <a name="mciwndm_openinterface-message"></a><span data-ttu-id="de18f-105">MCIWNDM \_ OPENINTERFACE</span><span class="sxs-lookup"><span data-stu-id="de18f-105">MCIWNDM\_OPENINTERFACE message</span></span>

<span data-ttu-id="de18f-106">El **mensaje \_ OPENINTERFACE de MCIWNDM** asocia el flujo de datos o el archivo asociado a la interfaz especificada a una ventana de MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="de18f-106">The **MCIWNDM\_OPENINTERFACE** message attaches the data stream or file associated with the specified interface to an MCIWnd window.</span></span> <span data-ttu-id="de18f-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) .</span><span class="sxs-lookup"><span data-stu-id="de18f-107">You can send this message explicitly or by using the [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macro.</span></span>


```C++
MCIWNDM_OPENINTERFACE 
wParam = 0; 
lParam = (LPARAM) (LPUNKNOWN) pUnk; 
```



## <a name="parameters"></a><span data-ttu-id="de18f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de18f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de18f-109"><span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*pUnk*</span><span class="sxs-lookup"><span data-stu-id="de18f-109"><span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*pUnk*</span></span>
</dt> <dd>

<span data-ttu-id="de18f-110">Puntero a una interfaz IAVI que señala a un archivo o a un flujo de datos de un archivo.</span><span class="sxs-lookup"><span data-stu-id="de18f-110">Pointer to an IAVI interface that points to a file or a data stream in a file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de18f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de18f-111">Return Value</span></span>

<span data-ttu-id="de18f-112">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="de18f-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="de18f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de18f-113">Requirements</span></span>



| <span data-ttu-id="de18f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="de18f-114">Requirement</span></span> | <span data-ttu-id="de18f-115">Value</span><span class="sxs-lookup"><span data-stu-id="de18f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="de18f-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de18f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="de18f-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="de18f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="de18f-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de18f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="de18f-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="de18f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="de18f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de18f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="de18f-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="de18f-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de18f-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="de18f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de18f-123">**MCIWndOpenInterface**</span><span class="sxs-lookup"><span data-stu-id="de18f-123">**MCIWndOpenInterface**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface)
</dt> </dl>

 

 





