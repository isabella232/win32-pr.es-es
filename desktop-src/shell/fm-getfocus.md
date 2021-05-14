---
description: Enviado por una extensión del Administrador de archivos para recuperar el tipo de ventana del Administrador de archivos que tiene el foco de entrada.
title: FM_GETFOCUS mensaje (Wfext.h)
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
ms.openlocfilehash: e5f6470ea1217485b401387150cae786b44ccca1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841416"
---
# <a name="fm_getfocus-message"></a><span data-ttu-id="afaa0-103">Mensaje \_ GETFOCUS de FM</span><span class="sxs-lookup"><span data-stu-id="afaa0-103">FM\_GETFOCUS message</span></span>

<span data-ttu-id="afaa0-104">Enviado por una extensión del Administrador de archivos para recuperar el tipo de ventana del Administrador de archivos que tiene el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="afaa0-104">Sent by a File Manager extension to retrieve the type of File Manager window that has the input focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="afaa0-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="afaa0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afaa0-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="afaa0-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="afaa0-107">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="afaa0-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="afaa0-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="afaa0-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="afaa0-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="afaa0-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afaa0-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="afaa0-110">Return value</span></span>

<span data-ttu-id="afaa0-111">Devuelve el tipo de ventana del Administrador de archivos que tiene el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="afaa0-111">Returns the type of File Manager window that has the input focus.</span></span> <span data-ttu-id="afaa0-112">Puede ser uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="afaa0-112">It can be one of the following values.</span></span>



| <span data-ttu-id="afaa0-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="afaa0-113">Return code</span></span>                                                                                    | <span data-ttu-id="afaa0-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="afaa0-114">Description</span></span>                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="afaa0-115"><dt>**FMFOCUS \_ DIR**</dt></span><span class="sxs-lookup"><span data-stu-id="afaa0-115"><dt>**FMFOCUS\_DIR**</dt></span></span> </dl>    | <span data-ttu-id="afaa0-116">Parte del directorio de una ventana de directorio.</span><span class="sxs-lookup"><span data-stu-id="afaa0-116">Directory portion of a directory window.</span></span><br/> |
| <dl> <span data-ttu-id="afaa0-117"><dt>**ÁRBOL \_ FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="afaa0-117"><dt>**FMFOCUS\_TREE**</dt></span></span> </dl>   | <span data-ttu-id="afaa0-118">Parte de árbol de una ventana de directorio.</span><span class="sxs-lookup"><span data-stu-id="afaa0-118">Tree portion of a directory window.</span></span><br/>      |
| <dl> <span data-ttu-id="afaa0-119"><dt>**UNIDADES \_ FMFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="afaa0-119"><dt>**FMFOCUS\_DRIVES**</dt></span></span> </dl> | <span data-ttu-id="afaa0-120">Barra de unidad de una ventana de directorio.</span><span class="sxs-lookup"><span data-stu-id="afaa0-120">Drive bar of a directory window.</span></span><br/>         |
| <dl> <span data-ttu-id="afaa0-121"><dt>**FMFOCUS \_ SEARCH**</dt></span><span class="sxs-lookup"><span data-stu-id="afaa0-121"><dt>**FMFOCUS\_SEARCH**</dt></span></span> </dl> | <span data-ttu-id="afaa0-122">Ventana Resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="afaa0-122">Search Results window.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="afaa0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afaa0-123">Requirements</span></span>



| <span data-ttu-id="afaa0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="afaa0-124">Requirement</span></span> | <span data-ttu-id="afaa0-125">Value</span><span class="sxs-lookup"><span data-stu-id="afaa0-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="afaa0-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="afaa0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="afaa0-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="afaa0-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="afaa0-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="afaa0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="afaa0-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="afaa0-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="afaa0-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afaa0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="afaa0-131"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="afaa0-131"><dt>Wfext.h</dt></span></span> </dl> |



 

 




