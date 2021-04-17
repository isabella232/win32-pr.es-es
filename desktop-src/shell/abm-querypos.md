---
description: Solicita un tamaño y una posición en la pantalla para un Appbar.
ms.assetid: 061a30fb-a68a-464e-ad8c-0bda672b57d9
title: Mensaje de ABM_QUERYPOS (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f25ef636b2c55d8442df49f86a59b537694c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360172"
---
# <a name="abm_querypos-message"></a><span data-ttu-id="ff76a-103">ABN \_ QUERYPOS</span><span class="sxs-lookup"><span data-stu-id="ff76a-103">ABM\_QUERYPOS message</span></span>

<span data-ttu-id="ff76a-104">Solicita un tamaño y una posición en la pantalla para un Appbar.</span><span class="sxs-lookup"><span data-stu-id="ff76a-104">Requests a size and screen position for an appbar.</span></span> <span data-ttu-id="ff76a-105">Cuando se realiza la solicitud, el mensaje propone un borde de pantalla y un rectángulo delimitador para el Appbar.</span><span class="sxs-lookup"><span data-stu-id="ff76a-105">When the request is made, the message proposes a screen edge and a bounding rectangle for the appbar.</span></span> <span data-ttu-id="ff76a-106">El sistema ajusta el rectángulo delimitador para que el Appbar no interfiera con la barra de tareas de Windows ni con ningún otro appbars.</span><span class="sxs-lookup"><span data-stu-id="ff76a-106">The system adjusts the bounding rectangle so that the appbar does not interfere with the Windows taskbar or any other appbars.</span></span>


```C++
SHAppBarMessage(ABM_QUERYPOS, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="ff76a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff76a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff76a-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="ff76a-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="ff76a-109">Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="ff76a-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="ff76a-110">El miembro **uEdge** especifica un borde de pantalla y el miembro **RC** contiene el rectángulo delimitador propuesto.</span><span class="sxs-lookup"><span data-stu-id="ff76a-110">The **uEdge** member specifies a screen edge, and the **rc** member contains the proposed bounding rectangle.</span></span> <span data-ttu-id="ff76a-111">Cuando la función [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) devuelve, **RC** contiene el rectángulo delimitador aprobado.</span><span class="sxs-lookup"><span data-stu-id="ff76a-111">When the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function returns, **rc** contains the approved bounding rectangle.</span></span> <span data-ttu-id="ff76a-112">Debe especificar los miembros **cbSize**, **hWnd**, **uEdge** y **RC** al enviar este mensaje. se omiten todos los demás miembros.</span><span class="sxs-lookup"><span data-stu-id="ff76a-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff76a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff76a-113">Return value</span></span>

<span data-ttu-id="ff76a-114">Siempre devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="ff76a-114">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff76a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff76a-115">Remarks</span></span>

<span data-ttu-id="ff76a-116">Un Appbar debe enviar este mensaje antes de enviar el mensaje [**\_ SETPOS de ABN**](abm-setpos.md) .</span><span class="sxs-lookup"><span data-stu-id="ff76a-116">An appbar should send this message before sending the [**ABM\_SETPOS**](abm-setpos.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff76a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff76a-117">Requirements</span></span>



| <span data-ttu-id="ff76a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff76a-118">Requirement</span></span> | <span data-ttu-id="ff76a-119">Value</span><span class="sxs-lookup"><span data-stu-id="ff76a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ff76a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff76a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ff76a-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ff76a-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ff76a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff76a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ff76a-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ff76a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ff76a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff76a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff76a-125"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff76a-125"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




