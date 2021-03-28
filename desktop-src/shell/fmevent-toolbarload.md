---
description: Se envía a un archivo DLL de extensión cuando el administrador de archivos está cargando su barra de herramientas. Este mensaje permite a un archivo DLL de extensión agregar un botón a la barra de herramientas del administrador de archivos.
title: Mensaje de FMEVENT_TOOLBARLOAD (Wfext. h)
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
ms.openlocfilehash: 5f04b524c8d44d987513b6605f9f827336078d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276760"
---
# <a name="fmevent_toolbarload-message"></a><span data-ttu-id="555d7-104">FMEVENT \_ TOOLBARLOAD</span><span class="sxs-lookup"><span data-stu-id="555d7-104">FMEVENT\_TOOLBARLOAD message</span></span>

<span data-ttu-id="555d7-105">Se envía a un archivo DLL de extensión cuando el administrador de archivos está cargando su barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="555d7-105">Sent to an extension DLL when File Manager is loading its toolbar.</span></span> <span data-ttu-id="555d7-106">Este mensaje permite a un archivo DLL de extensión agregar un botón a la barra de herramientas del administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="555d7-106">This message allows an extension DLL to add a button to the File Manager toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="555d7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="555d7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="555d7-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="555d7-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="555d7-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="555d7-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="555d7-110">*lpfmstbl*</span><span class="sxs-lookup"><span data-stu-id="555d7-110">*lpfmstbl*</span></span> 
</dt> <dd>

<span data-ttu-id="555d7-111">Dirección de una estructura [**de \_ TOOLBARLOAD de FMS**](fms-toolbarload.md) .</span><span class="sxs-lookup"><span data-stu-id="555d7-111">The address of an [**FMS\_TOOLBARLOAD**](fms-toolbarload.md) structure.</span></span> <span data-ttu-id="555d7-112">Si el archivo DLL de extensión agrega un botón a la barra de herramientas en el administrador de archivos, el archivo DLL debe rellenar la estructura con información acerca del botón.</span><span class="sxs-lookup"><span data-stu-id="555d7-112">If the extension DLL adds a button to the toolbar in File Manager, the DLL should fill the structure with information about the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="555d7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="555d7-113">Return value</span></span>

<span data-ttu-id="555d7-114">Un archivo DLL de extensión debe devolver **true** para agregar el botón a la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="555d7-114">An extension DLL must return **TRUE** to add the button to the toolbar.</span></span> <span data-ttu-id="555d7-115">Si el archivo DLL devuelve **false**, el administrador de archivos no agrega el botón.</span><span class="sxs-lookup"><span data-stu-id="555d7-115">If the DLL returns **FALSE**, File Manager does not add the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="555d7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="555d7-116">Requirements</span></span>



| <span data-ttu-id="555d7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="555d7-117">Requirement</span></span> | <span data-ttu-id="555d7-118">Value</span><span class="sxs-lookup"><span data-stu-id="555d7-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="555d7-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="555d7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="555d7-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="555d7-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="555d7-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="555d7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="555d7-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="555d7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="555d7-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="555d7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="555d7-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="555d7-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="555d7-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="555d7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="555d7-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="555d7-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




