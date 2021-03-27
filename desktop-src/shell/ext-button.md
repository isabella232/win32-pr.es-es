---
description: Contiene información sobre un botón que un archivo DLL de extensión del administrador de archivos agrega a la barra de herramientas del administrador de archivos.
title: EXT_BUTTON estructura (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXT_BUTTON
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8cd29a06-0f38-4285-9092-647a391b72d7
ms.openlocfilehash: 5eabb9f5e958b1e0bd15a6412dfbfa276d23f255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809410"
---
# <a name="ext_button-structure"></a><span data-ttu-id="fb686-103">\_Estructura del botón ext</span><span class="sxs-lookup"><span data-stu-id="fb686-103">EXT\_BUTTON structure</span></span>

<span data-ttu-id="fb686-104">Contiene información sobre un botón que un archivo DLL de extensión del administrador de archivos agrega a la barra de herramientas del administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="fb686-104">Contains information about a button that a File Manager extension DLL is adding to the toolbar of File Manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb686-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb686-105">Syntax</span></span>


```C++
typedef struct tagEXT_BUTTON {
  WORD idCommand;
  WORD idsHelp;
  WORD fsStyle;
} EXT_BUTTON, *LPEXT_BUTTON;
```



## <a name="members"></a><span data-ttu-id="fb686-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="fb686-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fb686-107">**idCommand**</span><span class="sxs-lookup"><span data-stu-id="fb686-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="fb686-108">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="fb686-108">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="fb686-109">Identificador de comando para el botón.</span><span class="sxs-lookup"><span data-stu-id="fb686-109">A command identifier for the button.</span></span>

</dd> <dt>

<span data-ttu-id="fb686-110">**idsHelp**</span><span class="sxs-lookup"><span data-stu-id="fb686-110">**idsHelp**</span></span>
</dt> <dd>

<span data-ttu-id="fb686-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="fb686-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="fb686-112">Identificador de la cadena de ayuda para el botón.</span><span class="sxs-lookup"><span data-stu-id="fb686-112">The identifier of the Help string for the button.</span></span>

</dd> <dt>

<span data-ttu-id="fb686-113">**fsStyle**</span><span class="sxs-lookup"><span data-stu-id="fb686-113">**fsStyle**</span></span>
</dt> <dd>

<span data-ttu-id="fb686-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="fb686-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="fb686-115">Estilo del botón.</span><span class="sxs-lookup"><span data-stu-id="fb686-115">The style of the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb686-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb686-116">Requirements</span></span>



| <span data-ttu-id="fb686-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb686-117">Requirement</span></span> | <span data-ttu-id="fb686-118">Value</span><span class="sxs-lookup"><span data-stu-id="fb686-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb686-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb686-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fb686-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fb686-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="fb686-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb686-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fb686-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fb686-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fb686-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb686-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb686-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb686-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb686-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb686-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb686-126">**FMEVENT \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="fb686-126">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> <dt>

[<span data-ttu-id="fb686-127">**TOOLBARLOAD de FMS \_**</span><span class="sxs-lookup"><span data-stu-id="fb686-127">**FMS\_TOOLBARLOAD**</span></span>](fms-toolbarload.md)
</dt> </dl>

 

 




