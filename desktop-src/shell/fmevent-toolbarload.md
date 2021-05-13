---
description: Se envía a un archivo DLL de extensión cuando el Administrador de archivos carga su barra de herramientas. Este mensaje permite que un archivo DLL de extensión agregue un botón a la barra de herramientas del Administrador de archivos.
title: FMEVENT_TOOLBARLOAD mensaje (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c5daab49-4ed5-439b-b1b7-a87f70c379f0
ms.openlocfilehash: c4195acedbd696679a2deea2f4d6e268717566d1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841276"
---
# <a name="fmevent_toolbarload-message"></a><span data-ttu-id="b29bd-104">MENSAJE DE DESCARGA \_ DE LA BARRA DE HERRAMIENTAS DE FMEVENT</span><span class="sxs-lookup"><span data-stu-id="b29bd-104">FMEVENT\_TOOLBARLOAD message</span></span>

<span data-ttu-id="b29bd-105">Se envía a un archivo DLL de extensión cuando el Administrador de archivos carga su barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="b29bd-105">Sent to an extension DLL when File Manager is loading its toolbar.</span></span> <span data-ttu-id="b29bd-106">Este mensaje permite que un archivo DLL de extensión agregue un botón a la barra de herramientas del Administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="b29bd-106">This message allows an extension DLL to add a button to the File Manager toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b29bd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b29bd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b29bd-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b29bd-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b29bd-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b29bd-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b29bd-110">*lpfmstbl*</span><span class="sxs-lookup"><span data-stu-id="b29bd-110">*lpfmstbl*</span></span> 
</dt> <dd>

<span data-ttu-id="b29bd-111">Dirección de una estructura [**\_ TOOLBARLOAD de FMS.**](fms-toolbarload.md)</span><span class="sxs-lookup"><span data-stu-id="b29bd-111">The address of an [**FMS\_TOOLBARLOAD**](fms-toolbarload.md) structure.</span></span> <span data-ttu-id="b29bd-112">Si el archivo DLL de extensión agrega un botón a la barra de herramientas del Administrador de archivos, el archivo DLL debe rellenar la estructura con información sobre el botón.</span><span class="sxs-lookup"><span data-stu-id="b29bd-112">If the extension DLL adds a button to the toolbar in File Manager, the DLL should fill the structure with information about the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b29bd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b29bd-113">Return value</span></span>

<span data-ttu-id="b29bd-114">Un archivo DLL de extensión debe devolver **TRUE** para agregar el botón a la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="b29bd-114">An extension DLL must return **TRUE** to add the button to the toolbar.</span></span> <span data-ttu-id="b29bd-115">Si el archivo DLL devuelve **FALSE,** el Administrador de archivos no agrega el botón.</span><span class="sxs-lookup"><span data-stu-id="b29bd-115">If the DLL returns **FALSE**, File Manager does not add the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="b29bd-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b29bd-116">Requirements</span></span>



| <span data-ttu-id="b29bd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b29bd-117">Requirement</span></span> | <span data-ttu-id="b29bd-118">Value</span><span class="sxs-lookup"><span data-stu-id="b29bd-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b29bd-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b29bd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b29bd-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b29bd-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b29bd-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b29bd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b29bd-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b29bd-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b29bd-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b29bd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b29bd-124"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="b29bd-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b29bd-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b29bd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b29bd-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="b29bd-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




