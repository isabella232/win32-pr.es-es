---
title: Mensaje de MCIWNDM_RETURNSTRING (VFW. h)
description: El \_ mensaje RETURNSTRING de MCIWNDM recupera la respuesta al comando de cadena MCI más reciente enviado a un dispositivo MCI.
ms.assetid: 36a5222c-a63c-4b8c-ad0c-a00477e95b96
keywords:
- Mensaje de MCIWNDM_RETURNSTRING de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_RETURNSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b99307bd7d61a70db594d0a696cceccd6d246a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079344"
---
# <a name="mciwndm_returnstring-message"></a><span data-ttu-id="f5f24-104">MCIWNDM \_ RETURNSTRING</span><span class="sxs-lookup"><span data-stu-id="f5f24-104">MCIWNDM\_RETURNSTRING message</span></span>

<span data-ttu-id="f5f24-105">El **mensaje \_ RETURNSTRING de MCIWNDM** recupera la respuesta al comando de cadena MCI más reciente enviado a un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="f5f24-105">The **MCIWNDM\_RETURNSTRING** message retrieves the reply to the most recent MCI string command sent to an MCI device.</span></span> <span data-ttu-id="f5f24-106">La información de la respuesta se proporciona como una cadena terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="f5f24-106">Information in the reply is supplied as a null-terminated string.</span></span> <span data-ttu-id="f5f24-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) .</span><span class="sxs-lookup"><span data-stu-id="f5f24-107">You can send this message explicitly or by using the [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) macro.</span></span>


```C++
MCIWNDM_RETURNSTRING 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="f5f24-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5f24-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5f24-109"><span id="len"></span><span id="LEN"></span>*terminado*</span><span class="sxs-lookup"><span data-stu-id="f5f24-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="f5f24-110">Tamaño, en bytes, del búfer.</span><span class="sxs-lookup"><span data-stu-id="f5f24-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f5f24-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="f5f24-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="f5f24-112">Puntero a un búfer definido por la aplicación que va a contener la cadena terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="f5f24-112">Pointer to an application-defined buffer to contain the null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5f24-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5f24-113">Return Value</span></span>

<span data-ttu-id="f5f24-114">Devuelve un entero que corresponde a la cadena MCI.</span><span class="sxs-lookup"><span data-stu-id="f5f24-114">Returns an integer corresponding to the MCI string.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5f24-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5f24-115">Remarks</span></span>

<span data-ttu-id="f5f24-116">Si la cadena terminada en NULL es más larga que el búfer, la cadena se trunca.</span><span class="sxs-lookup"><span data-stu-id="f5f24-116">If the null-terminated string is longer than the buffer, the string is truncated.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5f24-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5f24-117">Requirements</span></span>



| <span data-ttu-id="f5f24-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5f24-118">Requirement</span></span> | <span data-ttu-id="f5f24-119">Value</span><span class="sxs-lookup"><span data-stu-id="f5f24-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f5f24-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5f24-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f5f24-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f5f24-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f5f24-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5f24-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f5f24-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f5f24-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f5f24-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5f24-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5f24-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5f24-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5f24-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5f24-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5f24-127">**MCIWndReturnString**</span><span class="sxs-lookup"><span data-stu-id="f5f24-127">**MCIWndReturnString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
</dt> </dl>

 

 





