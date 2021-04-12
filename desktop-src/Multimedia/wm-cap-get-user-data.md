---
title: Mensaje de WM_CAP_GET_USER_DATA (VFW. h)
description: El \_ mensaje de datos del usuario Cap get de WM \_ \_ \_ recupera un \_ valor de datos PTR largo asociado a una ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro capGetUserData.
ms.assetid: f7c121ba-44a1-4916-b602-c53d8332c2af
keywords:
- Mensaje de WM_CAP_GET_USER_DATA de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02951667600acba115f506a610b167b72b69ea99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535020"
---
# <a name="wm_cap_get_user_data-message"></a><span data-ttu-id="4c187-105">\_Mensaje de \_ datos de usuario de obtención de Cap de \_ WM \_</span><span class="sxs-lookup"><span data-stu-id="4c187-105">WM\_CAP\_GET\_USER\_DATA message</span></span>

<span data-ttu-id="4c187-106">El mensaje de **\_ \_ datos del \_ usuario \_ Cap get de WM** recupera un valor de datos **\_ ptr largo** asociado a una ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="4c187-106">The **WM\_CAP\_GET\_USER\_DATA** message retrieves a **LONG\_PTR** data value associated with a capture window.</span></span> <span data-ttu-id="4c187-107">Puede enviar este mensaje explícitamente o mediante la macro [**capGetUserData**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) .</span><span class="sxs-lookup"><span data-stu-id="4c187-107">You can send this message explicitly or by using the [**capGetUserData**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) macro.</span></span>


```C++
WM_CAP_GET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="4c187-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c187-108">Return Value</span></span>

<span data-ttu-id="4c187-109">Devuelve un valor previamente guardado mediante el mensaje [**de \_ \_ datos del \_ usuario \_ del conjunto de límites de WM**](wm-cap-set-user-data.md) .</span><span class="sxs-lookup"><span data-stu-id="4c187-109">Returns a value previously saved by using the [**WM\_CAP\_SET\_USER\_DATA**](wm-cap-set-user-data.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c187-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c187-110">Requirements</span></span>



| <span data-ttu-id="4c187-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c187-111">Requirement</span></span> | <span data-ttu-id="4c187-112">Value</span><span class="sxs-lookup"><span data-stu-id="4c187-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4c187-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c187-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4c187-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4c187-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4c187-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c187-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4c187-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4c187-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4c187-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c187-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c187-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c187-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c187-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c187-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c187-120">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="4c187-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="4c187-121">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="4c187-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





