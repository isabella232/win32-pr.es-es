---
title: Mensaje de MCIWNDM_GETERROR (VFW. h)
description: El \_ mensaje MCIWNDM GETERROR recupera el último error de MCI encontrado. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetError.
ms.assetid: f110a9b3-5b05-4bf0-85d1-b49ce7396222
keywords:
- Mensaje de MCIWNDM_GETERROR de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c2977bb079351824b48da21f4ba3cc2dc5afe7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905055"
---
# <a name="mciwndm_geterror-message"></a><span data-ttu-id="d29d7-105">MCIWNDM \_ GETERROR</span><span class="sxs-lookup"><span data-stu-id="d29d7-105">MCIWNDM\_GETERROR message</span></span>

<span data-ttu-id="d29d7-106">El mensaje **MCIWNDM \_ GETERROR** recupera el último error de MCI encontrado.</span><span class="sxs-lookup"><span data-stu-id="d29d7-106">The **MCIWNDM\_GETERROR** message retrieves the last MCI error encountered.</span></span> <span data-ttu-id="d29d7-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) .</span><span class="sxs-lookup"><span data-stu-id="d29d7-107">You can send this message explicitly or by using the [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) macro.</span></span>


```C++
MCIWNDM_GETERROR 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="d29d7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d29d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d29d7-109"><span id="len"></span><span id="LEN"></span>*terminado*</span><span class="sxs-lookup"><span data-stu-id="d29d7-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="d29d7-110">Tamaño, en bytes, del búfer de errores.</span><span class="sxs-lookup"><span data-stu-id="d29d7-110">Size, in bytes, of the error buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d29d7-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="d29d7-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="d29d7-112">Puntero a un búfer definido por la aplicación que se usa para devolver la cadena de error.</span><span class="sxs-lookup"><span data-stu-id="d29d7-112">Pointer to an application-defined buffer used to return the error string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d29d7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d29d7-113">Return Value</span></span>

<span data-ttu-id="d29d7-114">Devuelve el valor de error de entero si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="d29d7-114">Returns the integer error value if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d29d7-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d29d7-115">Remarks</span></span>

<span data-ttu-id="d29d7-116">Si *LP* es un puntero válido, se devuelve en su búfer una cadena terminada en NULL correspondiente al error.</span><span class="sxs-lookup"><span data-stu-id="d29d7-116">If *lp* is a valid pointer, a null-terminated string corresponding to the error is returned in its buffer.</span></span> <span data-ttu-id="d29d7-117">Si la cadena de error es más larga que el búfer, MCIWnd lo trunca.</span><span class="sxs-lookup"><span data-stu-id="d29d7-117">If the error string is longer than the buffer, MCIWnd truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="d29d7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d29d7-118">Requirements</span></span>



| <span data-ttu-id="d29d7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d29d7-119">Requirement</span></span> | <span data-ttu-id="d29d7-120">Value</span><span class="sxs-lookup"><span data-stu-id="d29d7-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d29d7-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d29d7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d29d7-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d29d7-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d29d7-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d29d7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d29d7-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d29d7-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d29d7-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d29d7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d29d7-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d29d7-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d29d7-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d29d7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d29d7-128">**MCIWndGetError**</span><span class="sxs-lookup"><span data-stu-id="d29d7-128">**MCIWndGetError**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
</dt> </dl>

 

 





