---
description: Se envía a un archivo DLL de extensión cuando el usuario selecciona un nombre de archivo en la ventana Directorio del administrador de archivos o en la ventana Resultados de la búsqueda.
title: Mensaje de FMEVENT_SELCHANGE (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_SELCHANGE
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0773aa74-adf2-4e90-aead-2a9a981be3cb
ms.openlocfilehash: 4b05bca54f75bd48b5e710e31c31e5f0f56a2597
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539531"
---
# <a name="fmevent_selchange-message"></a><span data-ttu-id="f9b26-103">FMEVENT \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="f9b26-103">FMEVENT\_SELCHANGE message</span></span>

<span data-ttu-id="f9b26-104">Se envía a un archivo DLL de extensión cuando el usuario selecciona un nombre de archivo en la ventana Directorio del administrador de archivos o en la ventana Resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f9b26-104">Sent to an extension DLL when the user selects a file name in the File Manager directory window or Search Results window.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9b26-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9b26-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9b26-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9b26-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f9b26-107">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f9b26-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f9b26-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9b26-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f9b26-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f9b26-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9b26-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9b26-110">Return value</span></span>

<span data-ttu-id="f9b26-111">Un archivo DLL de extensión debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="f9b26-111">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9b26-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9b26-112">Remarks</span></span>

<span data-ttu-id="f9b26-113">Los cambios en la parte del árbol de la ventana del directorio no producen este mensaje.</span><span class="sxs-lookup"><span data-stu-id="f9b26-113">Changes in the tree portion of the directory window do not produce this message.</span></span>

<span data-ttu-id="f9b26-114">Dado que el usuario puede cambiar la selección muchas veces, el archivo DLL de extensión debe volver rápidamente después de procesar este mensaje para evitar ralentizar el proceso de selección del usuario.</span><span class="sxs-lookup"><span data-stu-id="f9b26-114">Because the user can change the selection many times, the extension DLL must return promptly after processing this message to avoid slowing the selection process for the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9b26-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9b26-115">Requirements</span></span>



| <span data-ttu-id="f9b26-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9b26-116">Requirement</span></span> | <span data-ttu-id="f9b26-117">Value</span><span class="sxs-lookup"><span data-stu-id="f9b26-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f9b26-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9b26-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f9b26-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f9b26-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f9b26-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9b26-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f9b26-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f9b26-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f9b26-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9b26-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9b26-123"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9b26-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9b26-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9b26-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9b26-125">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="f9b26-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




