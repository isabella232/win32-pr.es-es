---
description: Se envía a un procedimiento de archivo DLL de extensión del administrador de archivos cuando el administrador de archivos desea una cadena de ayuda para un elemento de comando de menú o barra de herramientas.
title: Mensaje de FMEVENT_HELPSTRING (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 55fb5bfe-2889-40e5-9798-85f63727e31f
ms.openlocfilehash: ae3be1953d4c8bbf70f8f17fcf34fcfb1ac583f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276761"
---
# <a name="fmevent_helpstring-message"></a><span data-ttu-id="602ce-103">FMEVENT el \_ mensaje de HELPSTRING</span><span class="sxs-lookup"><span data-stu-id="602ce-103">FMEVENT\_HELPSTRING message</span></span>

<span data-ttu-id="602ce-104">Se envía a un procedimiento de archivo DLL de extensión del administrador de archivos cuando el administrador de archivos desea una cadena de ayuda para un elemento de comando de menú o barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="602ce-104">Sent to a File Manager extension DLL procedure when File Manager wants a Help string for a menu or toolbar command item.</span></span>

## <a name="parameters"></a><span data-ttu-id="602ce-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="602ce-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="602ce-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="602ce-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="602ce-107">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="602ce-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="602ce-108">*lpfmshs*</span><span class="sxs-lookup"><span data-stu-id="602ce-108">*lpfmshs*</span></span> 
</dt> <dd>

<span data-ttu-id="602ce-109">La dirección de una estructura [**FMS \_ HELPSTRING**](fms-helpstring.md) que comunica los datos de la cadena de ayuda de los elementos de comando.</span><span class="sxs-lookup"><span data-stu-id="602ce-109">The address of an [**FMS\_HELPSTRING**](fms-helpstring.md) structure that communicates command item Help string data.</span></span> <span data-ttu-id="602ce-110">La estructura **FMS \_ HELPSTRING** identifica el elemento de comando para el que se desea una cadena de ayuda, junto con un identificador de su menú.</span><span class="sxs-lookup"><span data-stu-id="602ce-110">The **FMS\_HELPSTRING** structure identifies the command item for which a Help string is wanted, along with a handle to its menu.</span></span> <span data-ttu-id="602ce-111">Después, una aplicación escribe la cadena de ayuda adecuada en el miembro **szHelp** de la estructura **FMS \_ HELPSTRING** .</span><span class="sxs-lookup"><span data-stu-id="602ce-111">An application then writes the appropriate Help string to the **FMS\_HELPSTRING** structure's **szHelp** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="602ce-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="602ce-112">Return value</span></span>

<span data-ttu-id="602ce-113">Un procedimiento de archivo DLL de extensión debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="602ce-113">An extension DLL procedure should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="602ce-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="602ce-114">Requirements</span></span>



| <span data-ttu-id="602ce-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="602ce-115">Requirement</span></span> | <span data-ttu-id="602ce-116">Value</span><span class="sxs-lookup"><span data-stu-id="602ce-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="602ce-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="602ce-117">Minimum supported client</span></span><br/> | <span data-ttu-id="602ce-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="602ce-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="602ce-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="602ce-119">Minimum supported server</span></span><br/> | <span data-ttu-id="602ce-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="602ce-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="602ce-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="602ce-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="602ce-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="602ce-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="602ce-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="602ce-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="602ce-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="602ce-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="602ce-125">**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="602ce-125">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




