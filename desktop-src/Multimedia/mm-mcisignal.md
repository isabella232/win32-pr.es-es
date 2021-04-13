---
title: Mensaje de MM_MCISIGNAL (mmsystem. h)
description: El \_ mensaje mm MCISIGNAL se envía a una ventana para notificar a una aplicación que un dispositivo MCI ha alcanzado una posición definida en un comando de señal anterior (señal de MCI \_ ).
ms.assetid: 12512d23-9a89-4e38-9ec5-88845766f4f6
keywords:
- Mensaje de MM_MCISIGNAL de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MCISIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d42d4d39f31b82c7461a5bd8d8561b0da1b6bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422494"
---
# <a name="mm_mcisignal-message"></a><span data-ttu-id="320c6-104">\_Mensaje MCISIGNAL mm</span><span class="sxs-lookup"><span data-stu-id="320c6-104">MM\_MCISIGNAL message</span></span>

<span data-ttu-id="320c6-105">El mensaje **mm \_ MCISIGNAL** se envía a una ventana para notificar a una aplicación que un dispositivo MCI ha alcanzado una posición definida en un comando de [**señal**](signal.md) anterior ( [**\_ señal de MCI**](mci-signal.md)).</span><span class="sxs-lookup"><span data-stu-id="320c6-105">The **MM\_MCISIGNAL** message is sent to a window to notify an application that an MCI device has reached a position defined in a previous [**signal**](signal.md) ( [**MCI\_SIGNAL**](mci-signal.md)) command.</span></span>


```C++
MM_MCISIGNAL 
wParam = (WPARAM) wID      
lParam = (LONG) lUserParm  
```



## <a name="parameters"></a><span data-ttu-id="320c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="320c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="320c6-107"><span id="wID"></span><span id="wid"></span><span id="WID"></span>*wID*</span><span class="sxs-lookup"><span data-stu-id="320c6-107"><span id="wID"></span><span id="wid"></span><span id="WID"></span>*wID*</span></span>
</dt> <dd>

<span data-ttu-id="320c6-108">Identificador del dispositivo que inicia el mensaje de señal.</span><span class="sxs-lookup"><span data-stu-id="320c6-108">Identifier of the device initiating the signal message.</span></span>

</dd> <dt>

<span data-ttu-id="320c6-109"><span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*</span><span class="sxs-lookup"><span data-stu-id="320c6-109"><span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*</span></span>
</dt> <dd>

<span data-ttu-id="320c6-110">Valor pasado en el miembro **dwUserParm** de la estructura de parámetros de **señal de MCI \_ \_ \_ DGV** cuando el comando **Signal** ha definido esta función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="320c6-110">Value passed in the **dwUserParm** member of the **MCI\_DGV\_SIGNAL\_PARAMS** structure when the **signal** command has defined this callback function.</span></span> <span data-ttu-id="320c6-111">Como alternativa, podría contener el valor de la posición.</span><span class="sxs-lookup"><span data-stu-id="320c6-111">Alternatively, it might contain the position value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="320c6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="320c6-112">Requirements</span></span>



| <span data-ttu-id="320c6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="320c6-113">Requirement</span></span> | <span data-ttu-id="320c6-114">Value</span><span class="sxs-lookup"><span data-stu-id="320c6-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="320c6-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="320c6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="320c6-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="320c6-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="320c6-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="320c6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="320c6-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="320c6-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="320c6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="320c6-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="320c6-120"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="320c6-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="320c6-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="320c6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="320c6-122">MCI</span><span class="sxs-lookup"><span data-stu-id="320c6-122">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="320c6-123">Mensajes de MCI</span><span class="sxs-lookup"><span data-stu-id="320c6-123">MCI Messages</span></span>](mci-messages.md)
</dt> <dt>

[<span data-ttu-id="320c6-124">**marcar**</span><span class="sxs-lookup"><span data-stu-id="320c6-124">**signal**</span></span>](signal.md)
</dt> </dl>

 

 





