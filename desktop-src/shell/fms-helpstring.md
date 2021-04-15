---
description: Contiene información que utiliza el administrador de archivos para agregar una cadena de ayuda para un elemento de comando de menú o barra de herramientas.
title: FMS_HELPSTRING estructura (Wfext. h)
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
ms.openlocfilehash: c934409712ae740797eb3b5af0b55c50ff125342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997737"
---
# <a name="fms_helpstring-structure"></a><span data-ttu-id="38107-103">FMS \_ HELPSTRING (estructura)</span><span class="sxs-lookup"><span data-stu-id="38107-103">FMS\_HELPSTRING structure</span></span>

<span data-ttu-id="38107-104">Contiene información que utiliza el administrador de archivos para agregar una cadena de ayuda para un elemento de comando de menú o barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="38107-104">Contains information that File Manager uses to add a Help string for a menu or toolbar command item.</span></span>

## <a name="syntax"></a><span data-ttu-id="38107-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38107-105">Syntax</span></span>


```C++
typedef struct _FMS_HELPSTRING {
  INT       idCommand;
  HMENU     hMenu;
  __wchar_t szHelp[128];
} FMS_HELPSTRING;
```



## <a name="members"></a><span data-ttu-id="38107-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="38107-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="38107-107">**idCommand**</span><span class="sxs-lookup"><span data-stu-id="38107-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="38107-108">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="38107-108">Type: **INT**</span></span>

</dd> <dd>

<span data-ttu-id="38107-109">Identificador del elemento de comando.</span><span class="sxs-lookup"><span data-stu-id="38107-109">The identifier of the command item.</span></span>

</dd> <dt>

<span data-ttu-id="38107-110">**hMenu**</span><span class="sxs-lookup"><span data-stu-id="38107-110">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="38107-111">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="38107-111">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="38107-112">Identificador de la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="38107-112">The identifier of the menu bar.</span></span>

</dd> <dt>

<span data-ttu-id="38107-113">**szHelp**</span><span class="sxs-lookup"><span data-stu-id="38107-113">**szHelp**</span></span>
</dt> <dd>

<span data-ttu-id="38107-114">Tipo: **\_ \_ WCHAR \_ t \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="38107-114">Type: **\_\_wchar\_t\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="38107-115">Cadena terminada en null que recibe el texto de ayuda.</span><span class="sxs-lookup"><span data-stu-id="38107-115">The null-terminated string that receives the Help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38107-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38107-116">Requirements</span></span>



| <span data-ttu-id="38107-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="38107-117">Requirement</span></span> | <span data-ttu-id="38107-118">Value</span><span class="sxs-lookup"><span data-stu-id="38107-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="38107-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38107-119">Minimum supported client</span></span><br/> | <span data-ttu-id="38107-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="38107-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="38107-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38107-121">Minimum supported server</span></span><br/> | <span data-ttu-id="38107-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="38107-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="38107-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38107-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="38107-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="38107-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38107-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="38107-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38107-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="38107-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="38107-127">**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="38107-127">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




