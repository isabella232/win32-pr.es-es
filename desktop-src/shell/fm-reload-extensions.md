---
description: Enviado por una extensión del administrador de archivos (u otra aplicación) para que el administrador de archivos vuelva a cargar todos los archivos dll de extensión enumerados en la \[ \] sección de complementos del archivo de Winfile.ini.
ms.assetid: 5103a986-5f45-4deb-aaae-c6e87cb60051
title: Mensaje de FM_RELOAD_EXTENSIONS (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_RELOAD_EXTENSIONS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: 9e82ec9ec638cb70cc7b571ed9e5e76d604cd4da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985518"
---
# <a name="fm_reload_extensions-message"></a><span data-ttu-id="27b6b-103">Mensaje de extensión de \_ recarga de FM \_</span><span class="sxs-lookup"><span data-stu-id="27b6b-103">FM\_RELOAD\_EXTENSIONS message</span></span>

<span data-ttu-id="27b6b-104">Enviado por una extensión del administrador de archivos (u otra aplicación) para que el administrador de archivos vuelva a cargar todos los archivos dll de extensión enumerados en la \[ \] sección de complementos del archivo de Winfile.ini.</span><span class="sxs-lookup"><span data-stu-id="27b6b-104">Sent by a File Manager extension (or another application) to cause File Manager to reload all extension DLLs listed in the \[AddOns\] section of the Winfile.ini file.</span></span>

## <a name="parameters"></a><span data-ttu-id="27b6b-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27b6b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27b6b-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="27b6b-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27b6b-107">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="27b6b-107">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="27b6b-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27b6b-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27b6b-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="27b6b-109">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27b6b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27b6b-110">Return value</span></span>

<span data-ttu-id="27b6b-111">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="27b6b-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="27b6b-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27b6b-112">Remarks</span></span>

<span data-ttu-id="27b6b-113">Otras aplicaciones pueden usar la función [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) para enviar este mensaje al administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="27b6b-113">Other applications can use the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function to send this message to File Manager.</span></span> <span data-ttu-id="27b6b-114">Para obtener el identificador de ventana del administrador de archivos adecuado, una aplicación puede especificar "ft \_ frame" como el parámetro *lpszClassName* en una llamada a la función [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) .</span><span class="sxs-lookup"><span data-stu-id="27b6b-114">To obtain the appropriate File Manager window handle, an application can specify "WFS\_Frame" as the *lpszClassName* parameter in a call to the [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="27b6b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27b6b-115">Requirements</span></span>



| <span data-ttu-id="27b6b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="27b6b-116">Requirement</span></span> | <span data-ttu-id="27b6b-117">Value</span><span class="sxs-lookup"><span data-stu-id="27b6b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="27b6b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27b6b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="27b6b-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="27b6b-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="27b6b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27b6b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="27b6b-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="27b6b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="27b6b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27b6b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="27b6b-123"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="27b6b-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27b6b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="27b6b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27b6b-125">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="27b6b-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 
