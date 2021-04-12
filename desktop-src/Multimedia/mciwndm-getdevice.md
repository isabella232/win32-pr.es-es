---
title: Mensaje de MCIWNDM_GETDEVICE (VFW. h)
description: El \_ mensaje MCIWNDM GETDEVICE recupera el nombre del dispositivo MCI abierto actualmente. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetDevice.
ms.assetid: e69a73a6-a927-4536-98c7-ee7d5b16668a
keywords:
- Mensaje de MCIWNDM_GETDEVICE de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32664508a577db9d5a077e3cb4fd00aab34fbdf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489425"
---
# <a name="mciwndm_getdevice-message"></a><span data-ttu-id="2b3dc-105">MCIWNDM \_ GETDEVICE</span><span class="sxs-lookup"><span data-stu-id="2b3dc-105">MCIWNDM\_GETDEVICE message</span></span>

<span data-ttu-id="2b3dc-106">El mensaje **MCIWNDM \_ GETDEVICE** recupera el nombre del dispositivo MCI abierto actualmente.</span><span class="sxs-lookup"><span data-stu-id="2b3dc-106">The **MCIWNDM\_GETDEVICE** message retrieves the name of the currently open MCI device.</span></span> <span data-ttu-id="2b3dc-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) .</span><span class="sxs-lookup"><span data-stu-id="2b3dc-107">You can send this message explicitly or by using the [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) macro.</span></span>


```C++
MCIWNDM_GETDEVICE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="2b3dc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b3dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b3dc-109"><span id="len"></span><span id="LEN"></span>*terminado*</span><span class="sxs-lookup"><span data-stu-id="2b3dc-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="2b3dc-110">Tamaño, en bytes, del búfer.</span><span class="sxs-lookup"><span data-stu-id="2b3dc-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2b3dc-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="2b3dc-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="2b3dc-112">Puntero a un búfer definido por la aplicación para devolver el nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2b3dc-112">Pointer to an application-defined buffer to return the device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b3dc-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b3dc-113">Return Value</span></span>

<span data-ttu-id="2b3dc-114">Devuelve cero si es correcto o un valor distinto de cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2b3dc-114">Returns zero if successful or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b3dc-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b3dc-115">Remarks</span></span>

<span data-ttu-id="2b3dc-116">Si la cadena terminada en null que contiene el nombre del dispositivo es más larga que el búfer, MCIWnd lo trunca.</span><span class="sxs-lookup"><span data-stu-id="2b3dc-116">If the null-terminated string containing the device name is longer than the buffer, MCIWnd truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b3dc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b3dc-117">Requirements</span></span>



| <span data-ttu-id="2b3dc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b3dc-118">Requirement</span></span> | <span data-ttu-id="2b3dc-119">Value</span><span class="sxs-lookup"><span data-stu-id="2b3dc-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2b3dc-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b3dc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2b3dc-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2b3dc-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2b3dc-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b3dc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2b3dc-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2b3dc-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2b3dc-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b3dc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b3dc-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b3dc-125"><dt>Vfw.h</dt></span></span> </dl> |



 

 





