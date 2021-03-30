---
title: Mensaje de MCIWNDM_SENDSTRING (VFW. h)
description: El \_ mensaje MCIWNDM SENDSTRING envía un comando MCI en forma de cadena al dispositivo asociado a la ventana MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSendString.
ms.assetid: 0e999a0e-588d-4f06-a1bc-fd3f245d8980
keywords:
- Mensaje de MCIWNDM_SENDSTRING de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SENDSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36a034a3459803b1652bafed4eb389866add211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803014"
---
# <a name="mciwndm_sendstring-message"></a><span data-ttu-id="c9415-105">MCIWNDM \_ SENDSTRING</span><span class="sxs-lookup"><span data-stu-id="c9415-105">MCIWNDM\_SENDSTRING message</span></span>

<span data-ttu-id="c9415-106">El mensaje **MCIWNDM \_ SENDSTRING** envía un comando MCI en forma de cadena al dispositivo asociado a la ventana MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="c9415-106">The **MCIWNDM\_SENDSTRING** message sends an MCI command in string form to the device associated with the MCIWnd window.</span></span> <span data-ttu-id="c9415-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) .</span><span class="sxs-lookup"><span data-stu-id="c9415-107">You can send this message explicitly or by using the [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) macro.</span></span>


```C++
MCIWNDM_SENDSTRING 
wParam = 0; 
lParam = (LPARAM) (LPSTR) sz; 
```



## <a name="parameters"></a><span data-ttu-id="c9415-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9415-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9415-109"><span id="sz"></span><span id="SZ"></span>*SZ*</span><span class="sxs-lookup"><span data-stu-id="c9415-109"><span id="sz"></span><span id="SZ"></span>*sz*</span></span>
</dt> <dd>

<span data-ttu-id="c9415-110">Comando de cadena que se va a enviar al dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="c9415-110">String command to send to the MCI device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9415-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9415-111">Return Value</span></span>

<span data-ttu-id="c9415-112">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c9415-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9415-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9415-113">Remarks</span></span>

<span data-ttu-id="c9415-114">El controlador de mensajes de **MCIWNDM \_ SENDSTRING** anexa un alias de dispositivo al comando de MCI que se envía al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c9415-114">The message handler for **MCIWNDM\_SENDSTRING** appends a device alias to the MCI command you send to the device.</span></span> <span data-ttu-id="c9415-115">Por lo tanto, no debe usar ningún alias en un comando MCI que emita con **MCIWNDM \_ SENDSTRING**.</span><span class="sxs-lookup"><span data-stu-id="c9415-115">Therefore, you should not use any alias in an MCI command that you issue with **MCIWNDM\_SENDSTRING**.</span></span>

<span data-ttu-id="c9415-116">Para obtener la cadena devuelta, que contiene el resultado del comando, envíe el [**mensaje \_ RETURNSTRING de MCIWNDM**](mciwndm-returnstring.md) .</span><span class="sxs-lookup"><span data-stu-id="c9415-116">To get the return string, which contains the result of the command, send the [**MCIWNDM\_RETURNSTRING**](mciwndm-returnstring.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9415-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9415-117">Requirements</span></span>



| <span data-ttu-id="c9415-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9415-118">Requirement</span></span> | <span data-ttu-id="c9415-119">Value</span><span class="sxs-lookup"><span data-stu-id="c9415-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c9415-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9415-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c9415-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c9415-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c9415-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9415-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c9415-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c9415-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c9415-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9415-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9415-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9415-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9415-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9415-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9415-127">**MCIWndSendString**</span><span class="sxs-lookup"><span data-stu-id="c9415-127">**MCIWndSendString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)
</dt> <dt>

[<span data-ttu-id="c9415-128">Cadenas de comandos multimedia</span><span class="sxs-lookup"><span data-stu-id="c9415-128">Multimedia Command Strings</span></span>](multimedia-command-strings.md)
</dt> </dl>

 

 





