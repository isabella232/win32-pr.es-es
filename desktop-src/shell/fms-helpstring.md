---
description: Contiene información que el Administrador de archivos usa para agregar una cadena de Ayuda para un elemento de comando de menú o barra de herramientas.
title: FMS_HELPSTRING estructura (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b3ae7f86-5d58-47fa-87bd-e4e6a3541a93
ms.openlocfilehash: 4e9521df91619d108c7a03b6574926147fc2b04a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842216"
---
# <a name="fms_helpstring-structure"></a><span data-ttu-id="bece0-103">Estructura \_ HELPSTRING de FMS</span><span class="sxs-lookup"><span data-stu-id="bece0-103">FMS\_HELPSTRING structure</span></span>

<span data-ttu-id="bece0-104">Contiene información que el Administrador de archivos usa para agregar una cadena de Ayuda para un elemento de comando de menú o barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bece0-104">Contains information that File Manager uses to add a Help string for a menu or toolbar command item.</span></span>

## <a name="syntax"></a><span data-ttu-id="bece0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bece0-105">Syntax</span></span>


```C++
typedef struct _FMS_HELPSTRING {
  INT       idCommand;
  HMENU     hMenu;
  __wchar_t szHelp[128];
} FMS_HELPSTRING;
```



## <a name="members"></a><span data-ttu-id="bece0-106">Members</span><span class="sxs-lookup"><span data-stu-id="bece0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bece0-107">**idCommand**</span><span class="sxs-lookup"><span data-stu-id="bece0-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="bece0-108">Tipo: **INT**</span><span class="sxs-lookup"><span data-stu-id="bece0-108">Type: **INT**</span></span>

</dd> <dd>

<span data-ttu-id="bece0-109">Identificador del elemento de comando.</span><span class="sxs-lookup"><span data-stu-id="bece0-109">The identifier of the command item.</span></span>

</dd> <dt>

<span data-ttu-id="bece0-110">**hMenu**</span><span class="sxs-lookup"><span data-stu-id="bece0-110">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="bece0-111">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="bece0-111">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="bece0-112">Identificador de la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="bece0-112">The identifier of the menu bar.</span></span>

</dd> <dt>

<span data-ttu-id="bece0-113">**szHelp**</span><span class="sxs-lookup"><span data-stu-id="bece0-113">**szHelp**</span></span>
</dt> <dd>

<span data-ttu-id="bece0-114">Tipo: **\_ \_ wchar \_ t \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="bece0-114">Type: **\_\_wchar\_t\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="bece0-115">Cadena terminada en NULL que recibe el texto de ayuda.</span><span class="sxs-lookup"><span data-stu-id="bece0-115">The null-terminated string that receives the Help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bece0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bece0-116">Requirements</span></span>



| <span data-ttu-id="bece0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bece0-117">Requirement</span></span> | <span data-ttu-id="bece0-118">Value</span><span class="sxs-lookup"><span data-stu-id="bece0-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bece0-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bece0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bece0-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bece0-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="bece0-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bece0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bece0-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bece0-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bece0-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bece0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bece0-124"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="bece0-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bece0-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bece0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bece0-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="bece0-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="bece0-127">**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="bece0-127">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




