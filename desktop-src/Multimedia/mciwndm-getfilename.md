---
title: Mensaje de MCIWNDM_GETFILENAME (VFW. h)
description: El mensaje de MCIWNDM \_ GETFILENAME recupera el nombre de archivo que usa actualmente un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetFileName.
ms.assetid: d61b1b6d-0fae-4732-993c-41e08a4e05be
keywords:
- Mensaje de MCIWNDM_GETFILENAME de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETFILENAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 232a1d829b5cdd6da23e7dd3fb0294b95ca79f4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533813"
---
# <a name="mciwndm_getfilename-message"></a><span data-ttu-id="3a4d9-105">Mensaje de MCIWNDM \_ GETFILENAME</span><span class="sxs-lookup"><span data-stu-id="3a4d9-105">MCIWNDM\_GETFILENAME message</span></span>

<span data-ttu-id="3a4d9-106">El mensaje de **MCIWNDM \_ GETFILENAME** recupera el nombre de archivo que usa actualmente un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="3a4d9-106">The **MCIWNDM\_GETFILENAME** message retrieves the filename currently used by an MCI device.</span></span> <span data-ttu-id="3a4d9-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) .</span><span class="sxs-lookup"><span data-stu-id="3a4d9-107">You can send this message explicitly or by using the [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) macro.</span></span>


```C++
MCIWNDM_GETFILENAME 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="3a4d9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a4d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a4d9-109"><span id="len"></span><span id="LEN"></span>*terminado*</span><span class="sxs-lookup"><span data-stu-id="3a4d9-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="3a4d9-110">Tamaño, en bytes, del búfer.</span><span class="sxs-lookup"><span data-stu-id="3a4d9-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3a4d9-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="3a4d9-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="3a4d9-112">Puntero a un búfer definido por la aplicación para devolver el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="3a4d9-112">Pointer to an application-defined buffer to return the filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a4d9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a4d9-113">Return Value</span></span>

<span data-ttu-id="3a4d9-114">Devuelve cero si es correcto o 1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3a4d9-114">Returns zero if successful or 1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a4d9-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a4d9-115">Remarks</span></span>

<span data-ttu-id="3a4d9-116">Si la cadena terminada en null que contiene el nombre de archivo es más larga que el búfer, MCIWnd trunca el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="3a4d9-116">If the null-terminated string containing the filename is longer than the buffer, MCIWnd truncates the filename.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a4d9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a4d9-117">Requirements</span></span>



| <span data-ttu-id="3a4d9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a4d9-118">Requirement</span></span> | <span data-ttu-id="3a4d9-119">Value</span><span class="sxs-lookup"><span data-stu-id="3a4d9-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3a4d9-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a4d9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3a4d9-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3a4d9-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3a4d9-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a4d9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3a4d9-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3a4d9-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3a4d9-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a4d9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a4d9-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a4d9-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a4d9-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a4d9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a4d9-127">**MCIWndGetFileName**</span><span class="sxs-lookup"><span data-stu-id="3a4d9-127">**MCIWndGetFileName**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename)
</dt> </dl>

 

 





