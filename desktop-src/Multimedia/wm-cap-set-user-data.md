---
title: Mensaje de WM_CAP_SET_USER_DATA (VFW. h)
description: El mensaje de datos del usuario del conjunto de límites de WM \_ \_ \_ \_ asocia un valor largo de \_ datos PTR a una ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro capSetUserData.
ms.assetid: 067502e3-f009-4cf2-b612-4a0b64624416
keywords:
- Mensaje de WM_CAP_SET_USER_DATA de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542b8e49f740bfc265824947237841dede1f6065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151095"
---
# <a name="wm_cap_set_user_data-message"></a><span data-ttu-id="ddbdd-105">\_Mensaje de \_ datos de usuario del conjunto de Cap de \_ WM \_</span><span class="sxs-lookup"><span data-stu-id="ddbdd-105">WM\_CAP\_SET\_USER\_DATA message</span></span>

<span data-ttu-id="ddbdd-106">El mensaje de **datos del usuario del conjunto de límites de WM \_ \_ \_ \_** asocia un valor largo de datos **\_ ptr** a una ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="ddbdd-106">The **WM\_CAP\_SET\_USER\_DATA** message associates a **LONG\_PTR** data value with a capture window.</span></span> <span data-ttu-id="ddbdd-107">Puede enviar este mensaje explícitamente o mediante la macro [**capSetUserData**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) .</span><span class="sxs-lookup"><span data-stu-id="ddbdd-107">You can send this message explicitly or by using the [**capSetUserData**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) macro.</span></span>


```C++
WM_CAP_SET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = (LPARAM)lUser; 
```



## <a name="parameters"></a><span data-ttu-id="ddbdd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ddbdd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddbdd-109"><span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*lUser*</span><span class="sxs-lookup"><span data-stu-id="ddbdd-109"><span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*lUser*</span></span>
</dt> <dd>

<span data-ttu-id="ddbdd-110">Valor de datos que se va a asociar a una ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="ddbdd-110">Data value to associate with a capture window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddbdd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ddbdd-111">Return Value</span></span>

<span data-ttu-id="ddbdd-112">Devuelve **true** si es correcto o **false** si la captura de streaming está en curso.</span><span class="sxs-lookup"><span data-stu-id="ddbdd-112">Returns **TRUE** if successful or **FALSE** if streaming capture is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddbdd-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ddbdd-113">Remarks</span></span>

<span data-ttu-id="ddbdd-114">Normalmente, este mensaje se usa para señalar a un bloque de datos asociado a una ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="ddbdd-114">Typically this message is used to point to a block of data associated with a capture window.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddbdd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddbdd-115">Requirements</span></span>



| <span data-ttu-id="ddbdd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddbdd-116">Requirement</span></span> | <span data-ttu-id="ddbdd-117">Value</span><span class="sxs-lookup"><span data-stu-id="ddbdd-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ddbdd-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddbdd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ddbdd-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ddbdd-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ddbdd-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddbdd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ddbdd-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ddbdd-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ddbdd-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ddbdd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddbdd-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddbdd-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddbdd-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddbdd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddbdd-125">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="ddbdd-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="ddbdd-126">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="ddbdd-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





