---
description: Enviado por una extensión del administrador de archivos para recuperar la información de la unidad de la ventana del administrador de archivos activo.
title: Mensaje de FM_GETDRIVEINFO (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 142fff71-3a1b-4197-8c06-2e981cce4e4f
ms.openlocfilehash: 7accd78b36e82abbf56b02b133c79e92dd40d37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997220"
---
# <a name="fm_getdriveinfo-message"></a><span data-ttu-id="f8651-103">\_Mensaje GETDRIVEINFO de FM</span><span class="sxs-lookup"><span data-stu-id="f8651-103">FM\_GETDRIVEINFO message</span></span>

<span data-ttu-id="f8651-104">Enviado por una extensión del administrador de archivos para recuperar la información de la unidad de la ventana del administrador de archivos activo.</span><span class="sxs-lookup"><span data-stu-id="f8651-104">Sent by a File Manager extension to retrieve drive information from the active File Manager window.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8651-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8651-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8651-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8651-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f8651-107">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f8651-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f8651-108">*lpfmsgdi*</span><span class="sxs-lookup"><span data-stu-id="f8651-108">*lpfmsgdi*</span></span> 
</dt> <dd>

<span data-ttu-id="f8651-109">La dirección de una estructura de [**FMS \_ GETDRIVEINFO**](fms-getdriveinfo.md) que recibe información de la unidad.</span><span class="sxs-lookup"><span data-stu-id="f8651-109">The address of an [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure that receives drive information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8651-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8651-110">Return value</span></span>

<span data-ttu-id="f8651-111">Devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="f8651-111">Returns nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8651-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8651-112">Remarks</span></span>

<span data-ttu-id="f8651-113">Si se devuelve 0xFFFFFFFF en el miembro **dwTotalSpace** o **dwFreeSpace** de la estructura de [**FMS \_ GETDRIVEINFO**](fms-getdriveinfo.md) , la biblioteca de extensiones debe calcular el valor o los valores.</span><span class="sxs-lookup"><span data-stu-id="f8651-113">If 0xFFFFFFFF is returned in the **dwTotalSpace** or **dwFreeSpace** member of the [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure, the extension library must compute the value or values.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8651-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8651-114">Requirements</span></span>



| <span data-ttu-id="f8651-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8651-115">Requirement</span></span> | <span data-ttu-id="f8651-116">Value</span><span class="sxs-lookup"><span data-stu-id="f8651-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f8651-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8651-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f8651-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f8651-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f8651-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8651-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f8651-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f8651-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f8651-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8651-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8651-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8651-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8651-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8651-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8651-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="f8651-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




