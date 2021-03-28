---
description: Enviado por una extensión del administrador de archivos para recuperar el tipo de ventana del administrador de archivos que tiene el foco de entrada.
title: Mensaje de FM_GETFOCUS (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFOCUS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: e2d5f825-5678-4dd7-adad-eec1cbcc7e49
ms.openlocfilehash: af6e0894b3734f976302eacbf0575a017f054f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985527"
---
# <a name="fm_getfocus-message"></a><span data-ttu-id="51c88-103">\_Mensaje GETFOCUS de FM</span><span class="sxs-lookup"><span data-stu-id="51c88-103">FM\_GETFOCUS message</span></span>

<span data-ttu-id="51c88-104">Enviado por una extensión del administrador de archivos para recuperar el tipo de ventana del administrador de archivos que tiene el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="51c88-104">Sent by a File Manager extension to retrieve the type of File Manager window that has the input focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="51c88-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51c88-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51c88-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51c88-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="51c88-107">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="51c88-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="51c88-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51c88-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="51c88-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="51c88-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51c88-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51c88-110">Return value</span></span>

<span data-ttu-id="51c88-111">Devuelve el tipo de ventana del administrador de archivos que tiene el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="51c88-111">Returns the type of File Manager window that has the input focus.</span></span> <span data-ttu-id="51c88-112">Puede ser uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="51c88-112">It can be one of the following values.</span></span>



| <span data-ttu-id="51c88-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="51c88-113">Return code</span></span>                                                                                    | <span data-ttu-id="51c88-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="51c88-114">Description</span></span>                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="51c88-115"><dt>**FMFOCUS \_ dir**</dt></span><span class="sxs-lookup"><span data-stu-id="51c88-115"><dt>**FMFOCUS\_DIR**</dt></span></span> </dl>    | <span data-ttu-id="51c88-116">Parte del directorio de una ventana de directorio.</span><span class="sxs-lookup"><span data-stu-id="51c88-116">Directory portion of a directory window.</span></span><br/> |
| <dl> <span data-ttu-id="51c88-117"><dt>**\_árbol FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="51c88-117"><dt>**FMFOCUS\_TREE**</dt></span></span> </dl>   | <span data-ttu-id="51c88-118">Parte de árbol de una ventana de directorio.</span><span class="sxs-lookup"><span data-stu-id="51c88-118">Tree portion of a directory window.</span></span><br/>      |
| <dl> <span data-ttu-id="51c88-119"><dt>**\_unidades FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="51c88-119"><dt>**FMFOCUS\_DRIVES**</dt></span></span> </dl> | <span data-ttu-id="51c88-120">Barra de unidad de una ventana de directorio.</span><span class="sxs-lookup"><span data-stu-id="51c88-120">Drive bar of a directory window.</span></span><br/>         |
| <dl> <span data-ttu-id="51c88-121"><dt>**búsqueda de FMFOCUS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="51c88-121"><dt>**FMFOCUS\_SEARCH**</dt></span></span> </dl> | <span data-ttu-id="51c88-122">Ventana Resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="51c88-122">Search Results window.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="51c88-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51c88-123">Requirements</span></span>



| <span data-ttu-id="51c88-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="51c88-124">Requirement</span></span> | <span data-ttu-id="51c88-125">Value</span><span class="sxs-lookup"><span data-stu-id="51c88-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="51c88-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51c88-126">Minimum supported client</span></span><br/> | <span data-ttu-id="51c88-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="51c88-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="51c88-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51c88-128">Minimum supported server</span></span><br/> | <span data-ttu-id="51c88-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="51c88-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="51c88-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51c88-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="51c88-131"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="51c88-131"><dt>Wfext.h</dt></span></span> </dl> |



 

 




