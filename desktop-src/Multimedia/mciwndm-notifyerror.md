---
title: Mensaje de MCIWNDM_NOTIFYERROR (VFW. h)
description: El \_ mensaje MCIWNDM NOTIFYERROR notifica a la ventana primaria de una aplicación que se ha producido un error de MCI.
ms.assetid: 0f54886a-77dc-43cc-be46-2d322c75471a
keywords:
- Mensaje de MCIWNDM_NOTIFYERROR de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbef9180c31091f3bd1a85f23a08990c2f7e7ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079243"
---
# <a name="mciwndm_notifyerror-message"></a><span data-ttu-id="db34a-104">MCIWNDM \_ NOTIFYERROR</span><span class="sxs-lookup"><span data-stu-id="db34a-104">MCIWNDM\_NOTIFYERROR message</span></span>

<span data-ttu-id="db34a-105">El mensaje **MCIWNDM \_ NOTIFYERROR** notifica a la ventana primaria de una aplicación que se ha producido un error de MCI.</span><span class="sxs-lookup"><span data-stu-id="db34a-105">The **MCIWNDM\_NOTIFYERROR** message notifies the parent window of an application that an MCI error occurred.</span></span>


```C++
MCIWNDM_NOTIFYERROR 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) errorCode; 
```



## <a name="parameters"></a><span data-ttu-id="db34a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db34a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db34a-107"><span id="hwnd"></span><span id="HWND"></span>*identificador*</span><span class="sxs-lookup"><span data-stu-id="db34a-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="db34a-108">Identificador de la ventana de MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="db34a-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="db34a-109"><span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*errorCode*</span><span class="sxs-lookup"><span data-stu-id="db34a-109"><span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*errorCode*</span></span>
</dt> <dd>

<span data-ttu-id="db34a-110">Código numérico para el error de MCI.</span><span class="sxs-lookup"><span data-stu-id="db34a-110">Numerical code for the MCI error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db34a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db34a-111">Remarks</span></span>

<span data-ttu-id="db34a-112">Puede habilitar la notificación de error de MCI especificando el \_ estilo de ventana de MCIWNDF NOTIFYERROR.</span><span class="sxs-lookup"><span data-stu-id="db34a-112">You can enable MCI error notification by specifying the MCIWNDF\_NOTIFYERROR window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="db34a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db34a-113">Requirements</span></span>



| <span data-ttu-id="db34a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="db34a-114">Requirement</span></span> | <span data-ttu-id="db34a-115">Value</span><span class="sxs-lookup"><span data-stu-id="db34a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="db34a-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db34a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="db34a-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="db34a-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="db34a-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db34a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="db34a-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="db34a-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="db34a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db34a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="db34a-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="db34a-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 





