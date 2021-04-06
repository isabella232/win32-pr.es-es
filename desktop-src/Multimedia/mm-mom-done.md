---
title: Mensaje de MM_MOM_DONE (mmsystem. h)
description: El mensaje de MM \_ MOM \_ done se envía a una ventana cuando se ha reproducido el búfer de secuencia o exclusivo del sistema MIDI especificado y se va a devolver a la aplicación.
ms.assetid: 4651d5b4-3c98-4fa7-b761-dafb30e0d31e
keywords:
- Mensaje de MM_MOM_DONE de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ad5d4a7e91cc05aa51017cba79418b34445362
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078976"
---
# <a name="mm_mom_done-message"></a><span data-ttu-id="13cdb-104">Mensaje de MM \_ MOM \_ Done</span><span class="sxs-lookup"><span data-stu-id="13cdb-104">MM\_MOM\_DONE message</span></span>

<span data-ttu-id="13cdb-105">El mensaje de **mm \_ MOM \_ Done** se envía a una ventana cuando se ha reproducido el búfer de secuencia o exclusivo del sistema MIDI especificado y se va a devolver a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="13cdb-105">The **MM\_MOM\_DONE** message is sent to a window when the specified MIDI system-exclusive or stream buffer has been played and is being returned to the application.</span></span>


```C++
MM_MOM_DONE 
wParam = (WPARAM) hOutput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="13cdb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13cdb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13cdb-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span><span class="sxs-lookup"><span data-stu-id="13cdb-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="13cdb-108">Identificador del dispositivo de salida MIDI que reprodujo el búfer.</span><span class="sxs-lookup"><span data-stu-id="13cdb-108">Handle to the MIDI output device that played the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="13cdb-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="13cdb-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="13cdb-110">Puntero a una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el búfer.</span><span class="sxs-lookup"><span data-stu-id="13cdb-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13cdb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13cdb-111">Return Value</span></span>

<span data-ttu-id="13cdb-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="13cdb-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="13cdb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13cdb-113">Requirements</span></span>



| <span data-ttu-id="13cdb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="13cdb-114">Requirement</span></span> | <span data-ttu-id="13cdb-115">Value</span><span class="sxs-lookup"><span data-stu-id="13cdb-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13cdb-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13cdb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="13cdb-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="13cdb-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="13cdb-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13cdb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="13cdb-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="13cdb-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="13cdb-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13cdb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="13cdb-121"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13cdb-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13cdb-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="13cdb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13cdb-123">Mensajes MIDI</span><span class="sxs-lookup"><span data-stu-id="13cdb-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

