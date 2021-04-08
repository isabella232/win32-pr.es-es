---
title: Mensaje de MCIWNDM_NOTIFYMODE (VFW. h)
description: El \_ mensaje MCIWNDM NOTIFYMODE notifica a la ventana primaria de una aplicación que el modo de funcionamiento del dispositivo MCI ha cambiado.
ms.assetid: 08adfa8b-4d88-4953-acd8-8a4728f9e1b6
keywords:
- Mensaje de MCIWNDM_NOTIFYMODE de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fe75048a53023dab67bef4048d6149438ad54d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078838"
---
# <a name="mciwndm_notifymode-message"></a><span data-ttu-id="13e49-104">MCIWNDM \_ NOTIFYMODE</span><span class="sxs-lookup"><span data-stu-id="13e49-104">MCIWNDM\_NOTIFYMODE message</span></span>

<span data-ttu-id="13e49-105">El mensaje **MCIWNDM \_ NOTIFYMODE** notifica a la ventana primaria de una aplicación que el modo de funcionamiento del dispositivo MCI ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="13e49-105">The **MCIWNDM\_NOTIFYMODE** message notifies the parent window of an application that the operating mode of the MCI device has changed.</span></span>


```C++
MCIWNDM_NOTIFYMODE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) mode; 
```



## <a name="parameters"></a><span data-ttu-id="13e49-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13e49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13e49-107"><span id="hwnd"></span><span id="HWND"></span>*identificador*</span><span class="sxs-lookup"><span data-stu-id="13e49-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="13e49-108">Identificador de la ventana de MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="13e49-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="13e49-109"><span id="mode"></span><span id="MODE"></span>*modo*</span><span class="sxs-lookup"><span data-stu-id="13e49-109"><span id="mode"></span><span id="MODE"></span>*mode*</span></span>
</dt> <dd>

<span data-ttu-id="13e49-110">Entero que corresponde al modo MCI.</span><span class="sxs-lookup"><span data-stu-id="13e49-110">Integer corresponding to the MCI mode.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13e49-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13e49-111">Remarks</span></span>

<span data-ttu-id="13e49-112">Puede habilitar la notificación de cambios de modo de un dispositivo MCI especificando el estilo de ventana de MCIWNDF \_ NOTIFYMODE.</span><span class="sxs-lookup"><span data-stu-id="13e49-112">You can enable notification of mode changes of an MCI device by specifying the MCIWNDF\_NOTIFYMODE window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="13e49-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13e49-113">Requirements</span></span>



| <span data-ttu-id="13e49-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="13e49-114">Requirement</span></span> | <span data-ttu-id="13e49-115">Value</span><span class="sxs-lookup"><span data-stu-id="13e49-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="13e49-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13e49-116">Minimum supported client</span></span><br/> | <span data-ttu-id="13e49-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="13e49-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="13e49-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13e49-118">Minimum supported server</span></span><br/> | <span data-ttu-id="13e49-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="13e49-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="13e49-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13e49-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="13e49-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="13e49-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 





