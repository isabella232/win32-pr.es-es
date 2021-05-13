---
description: Se envía a un procedimiento DLL de extensión del Administrador de archivos cuando el Administrador de archivos quiere una cadena de Ayuda para un elemento de comando de menú o barra de herramientas.
title: FMEVENT_HELPSTRING mensaje (Wfext.h)
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
ms.openlocfilehash: 6fe187330e27f7e246c9bbd68005f68f346bbc90
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841286"
---
# <a name="fmevent_helpstring-message"></a><span data-ttu-id="a7b5d-103">Mensaje \_ HELPSTRING de FMEVENT</span><span class="sxs-lookup"><span data-stu-id="a7b5d-103">FMEVENT\_HELPSTRING message</span></span>

<span data-ttu-id="a7b5d-104">Se envía a un procedimiento DLL de extensión del Administrador de archivos cuando el Administrador de archivos quiere una cadena de Ayuda para un elemento de comando de menú o barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="a7b5d-104">Sent to a File Manager extension DLL procedure when File Manager wants a Help string for a menu or toolbar command item.</span></span>

## <a name="parameters"></a><span data-ttu-id="a7b5d-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7b5d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7b5d-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a7b5d-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a7b5d-107">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a7b5d-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a7b5d-108">*lpfmshs*</span><span class="sxs-lookup"><span data-stu-id="a7b5d-108">*lpfmshs*</span></span> 
</dt> <dd>

<span data-ttu-id="a7b5d-109">Dirección de una estructura [**\_ HELPSTRING de FMS**](fms-helpstring.md) que comunica los datos de la cadena de ayuda del elemento de comando.</span><span class="sxs-lookup"><span data-stu-id="a7b5d-109">The address of an [**FMS\_HELPSTRING**](fms-helpstring.md) structure that communicates command item Help string data.</span></span> <span data-ttu-id="a7b5d-110">La **estructura \_ HELPSTRING de FMS** identifica el elemento de comando para el que se desea una cadena de Ayuda, junto con un identificador para su menú.</span><span class="sxs-lookup"><span data-stu-id="a7b5d-110">The **FMS\_HELPSTRING** structure identifies the command item for which a Help string is wanted, along with a handle to its menu.</span></span> <span data-ttu-id="a7b5d-111">A continuación, una aplicación escribe la cadena de Ayuda adecuada en el miembro szHelp de la estructura **\_ HELPSTRING** **de FMS.**</span><span class="sxs-lookup"><span data-stu-id="a7b5d-111">An application then writes the appropriate Help string to the **FMS\_HELPSTRING** structure's **szHelp** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7b5d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7b5d-112">Return value</span></span>

<span data-ttu-id="a7b5d-113">Un procedimiento DLL de extensión debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="a7b5d-113">An extension DLL procedure should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7b5d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7b5d-114">Requirements</span></span>



| <span data-ttu-id="a7b5d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7b5d-115">Requirement</span></span> | <span data-ttu-id="a7b5d-116">Value</span><span class="sxs-lookup"><span data-stu-id="a7b5d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a7b5d-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7b5d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a7b5d-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a7b5d-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="a7b5d-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7b5d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a7b5d-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a7b5d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a7b5d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7b5d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7b5d-122"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="a7b5d-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7b5d-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a7b5d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7b5d-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="a7b5d-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="a7b5d-125">**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="a7b5d-125">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




