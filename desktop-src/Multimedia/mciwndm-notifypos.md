---
title: Mensaje de MCIWNDM_NOTIFYPOS (VFW. h)
description: El \_ mensaje MCIWNDM NOTIFYPOS notifica a la ventana primaria de una aplicación que ha cambiado la posición de la ventana.
ms.assetid: ccc8903b-ad79-495a-8003-20e120ad28ff
keywords:
- Mensaje de MCIWNDM_NOTIFYPOS de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYPOS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bebb3a8facd6478c21888cf0cf5ca81e3735ff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996894"
---
# <a name="mciwndm_notifypos-message"></a><span data-ttu-id="498c5-104">MCIWNDM \_ NOTIFYPOS</span><span class="sxs-lookup"><span data-stu-id="498c5-104">MCIWNDM\_NOTIFYPOS message</span></span>

<span data-ttu-id="498c5-105">El mensaje **MCIWNDM \_ NOTIFYPOS** notifica a la ventana primaria de una aplicación que ha cambiado la posición de la ventana.</span><span class="sxs-lookup"><span data-stu-id="498c5-105">The **MCIWNDM\_NOTIFYPOS** message notifies the parent window of an application that the window position has changed.</span></span>


```C++
MCIWNDM_NOTIFYPOS 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) pos; 
```



## <a name="parameters"></a><span data-ttu-id="498c5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="498c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="498c5-107"><span id="hwnd"></span><span id="HWND"></span>*identificador*</span><span class="sxs-lookup"><span data-stu-id="498c5-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="498c5-108">Identificador de la ventana de MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="498c5-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="498c5-109"><span id="pos"></span><span id="POS"></span>*abre*</span><span class="sxs-lookup"><span data-stu-id="498c5-109"><span id="pos"></span><span id="POS"></span>*pos*</span></span>
</dt> <dd>

<span data-ttu-id="498c5-110">Describe la nueva posición.</span><span class="sxs-lookup"><span data-stu-id="498c5-110">Describes the new position.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="498c5-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="498c5-111">Remarks</span></span>

<span data-ttu-id="498c5-112">Puede habilitar la notificación de cambios en la posición de una ventana de MCIWnd especificando el estilo de ventana de MCIWNDF \_ NOTIFYPOS.</span><span class="sxs-lookup"><span data-stu-id="498c5-112">You can enable notification of changes in the position of an MCIWnd window by specifying the MCIWNDF\_NOTIFYPOS window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="498c5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="498c5-113">Requirements</span></span>



| <span data-ttu-id="498c5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="498c5-114">Requirement</span></span> | <span data-ttu-id="498c5-115">Value</span><span class="sxs-lookup"><span data-stu-id="498c5-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="498c5-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="498c5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="498c5-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="498c5-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="498c5-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="498c5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="498c5-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="498c5-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="498c5-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="498c5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="498c5-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="498c5-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 





