---
title: Mensaje de MOM_DONE (Mciapi. h)
description: El \_ mensaje MOM done se envía a una función de devolución de llamada de salida MIDI cuando se ha reproducido el búfer de secuencia o exclusivo del sistema especificado y se va a devolver a la aplicación.
ms.assetid: 0b9bd0e1-c87d-4f21-912e-5ac9f5c04192
keywords:
- Mensaje de MOM_DONE de Windows multimedia
topic_type:
- apiref
api_name:
- MOM_DONE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af3f58f7d8f4625971dde5d7ec807c9f963d40f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422181"
---
# <a name="mom_done-message"></a><span data-ttu-id="75ad0-104">Mensaje de MOM \_ Done</span><span class="sxs-lookup"><span data-stu-id="75ad0-104">MOM\_DONE message</span></span>

<span data-ttu-id="75ad0-105">El mensaje **MOM \_ Done** se envía a una función de devolución de llamada de salida MIDI cuando se ha reproducido el búfer de secuencia o exclusivo del sistema especificado y se va a devolver a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="75ad0-105">The **MOM\_DONE** message is sent to a MIDI output callback function when the specified system-exclusive or stream buffer has been played and is being returned to the application.</span></span>


```C++
MOM_DONE 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="75ad0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75ad0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75ad0-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="75ad0-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="75ad0-108">Puntero a una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el búfer.</span><span class="sxs-lookup"><span data-stu-id="75ad0-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="75ad0-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="75ad0-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="75ad0-110">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="75ad0-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75ad0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75ad0-111">Return Value</span></span>

<span data-ttu-id="75ad0-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="75ad0-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="75ad0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75ad0-113">Requirements</span></span>



| <span data-ttu-id="75ad0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="75ad0-114">Requirement</span></span> | <span data-ttu-id="75ad0-115">Value</span><span class="sxs-lookup"><span data-stu-id="75ad0-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="75ad0-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75ad0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="75ad0-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="75ad0-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="75ad0-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75ad0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="75ad0-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="75ad0-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="75ad0-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75ad0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="75ad0-121"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="75ad0-121"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75ad0-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="75ad0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75ad0-123">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="75ad0-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

