---
description: Enviado por una extensión del Administrador de archivos para recuperar información de unidad desde la ventana activa del Administrador de archivos.
title: FM_GETDRIVEINFO mensaje (Wfext.h)
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
ms.openlocfilehash: 0abac794ed23eca30676a839a6eb5ad7c1079c3c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842416"
---
# <a name="fm_getdriveinfo-message"></a><span data-ttu-id="fbff9-103">Mensaje \_ GETDRIVEINFO de FM</span><span class="sxs-lookup"><span data-stu-id="fbff9-103">FM\_GETDRIVEINFO message</span></span>

<span data-ttu-id="fbff9-104">Enviado por una extensión del Administrador de archivos para recuperar información de unidad desde la ventana activa del Administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="fbff9-104">Sent by a File Manager extension to retrieve drive information from the active File Manager window.</span></span>

## <a name="parameters"></a><span data-ttu-id="fbff9-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fbff9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbff9-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fbff9-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fbff9-107">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fbff9-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fbff9-108">*lpfmsgdi*</span><span class="sxs-lookup"><span data-stu-id="fbff9-108">*lpfmsgdi*</span></span> 
</dt> <dd>

<span data-ttu-id="fbff9-109">Dirección de una estructura [**\_ GETDRIVEINFO de FMS**](fms-getdriveinfo.md) que recibe información de unidad.</span><span class="sxs-lookup"><span data-stu-id="fbff9-109">The address of an [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure that receives drive information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbff9-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fbff9-110">Return value</span></span>

<span data-ttu-id="fbff9-111">Devuelve distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="fbff9-111">Returns nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbff9-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fbff9-112">Remarks</span></span>

<span data-ttu-id="fbff9-113">Si 0xFFFFFFFF en el **miembro dwTotalSpace** o **dwFreeSpace** de la estructura [**\_ GETDRIVEINFO de FMS,**](fms-getdriveinfo.md) la biblioteca de extensiones debe calcular el valor o los valores.</span><span class="sxs-lookup"><span data-stu-id="fbff9-113">If 0xFFFFFFFF is returned in the **dwTotalSpace** or **dwFreeSpace** member of the [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure, the extension library must compute the value or values.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbff9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbff9-114">Requirements</span></span>



| <span data-ttu-id="fbff9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbff9-115">Requirement</span></span> | <span data-ttu-id="fbff9-116">Value</span><span class="sxs-lookup"><span data-stu-id="fbff9-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fbff9-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbff9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fbff9-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fbff9-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="fbff9-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbff9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fbff9-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fbff9-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fbff9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fbff9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbff9-122"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="fbff9-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbff9-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fbff9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbff9-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="fbff9-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




