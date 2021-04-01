---
title: Mensaje de MCIWNDM_NOTIFYSIZE (VFW. h)
description: El \_ mensaje MCIWNDM NOTIFYSIZE notifica a la ventana primaria de una aplicación que el tamaño de la ventana ha cambiado.
ms.assetid: 76e1f663-bfc6-4d3c-9486-c8c7f79e4265
keywords:
- Mensaje de MCIWNDM_NOTIFYSIZE de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYSIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59db02d69302127937a7203729de9cc8b98a58f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150170"
---
# <a name="mciwndm_notifysize-message"></a><span data-ttu-id="54875-104">MCIWNDM \_ NOTIFYSIZE</span><span class="sxs-lookup"><span data-stu-id="54875-104">MCIWNDM\_NOTIFYSIZE message</span></span>

<span data-ttu-id="54875-105">El mensaje **MCIWNDM \_ NOTIFYSIZE** notifica a la ventana primaria de una aplicación que el tamaño de la ventana ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="54875-105">The **MCIWNDM\_NOTIFYSIZE** message notifies the parent window of an application that the window size has changed.</span></span>


```C++
MCIWNDM_NOTIFYSIZE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="54875-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54875-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54875-107"><span id="hwnd"></span><span id="HWND"></span>*identificador*</span><span class="sxs-lookup"><span data-stu-id="54875-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="54875-108">Identificador de la ventana de MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="54875-108">Handle to the MCIWnd window.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54875-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54875-109">Remarks</span></span>

<span data-ttu-id="54875-110">Puede habilitar la notificación de cambios en el tamaño de una ventana de MCIWnd especificando el estilo de ventana de MCIWNDF \_ NOTIFYSIZE.</span><span class="sxs-lookup"><span data-stu-id="54875-110">You can enable notification of changes in the size of an MCIWnd window by specifying the MCIWNDF\_NOTIFYSIZE window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="54875-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54875-111">Requirements</span></span>



| <span data-ttu-id="54875-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="54875-112">Requirement</span></span> | <span data-ttu-id="54875-113">Value</span><span class="sxs-lookup"><span data-stu-id="54875-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="54875-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54875-114">Minimum supported client</span></span><br/> | <span data-ttu-id="54875-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="54875-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="54875-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54875-116">Minimum supported server</span></span><br/> | <span data-ttu-id="54875-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="54875-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="54875-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54875-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="54875-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="54875-119"><dt>Vfw.h</dt></span></span> </dl> |



 

 





