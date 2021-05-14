---
description: Contiene información sobre un botón que un archivo DLL de extensión del Administrador de archivos está agregando a la barra de herramientas del Administrador de archivos.
title: EXT_BUTTON estructura (Wfext.h)
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
ms.openlocfilehash: 6d1505ef7b330f0e935136eacaf808da3add8cd8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843156"
---
# <a name="ext_button-structure"></a><span data-ttu-id="98af6-103">EXT \_ BUTTON (estructura)</span><span class="sxs-lookup"><span data-stu-id="98af6-103">EXT\_BUTTON structure</span></span>

<span data-ttu-id="98af6-104">Contiene información sobre un botón que un archivo DLL de extensión del Administrador de archivos está agregando a la barra de herramientas del Administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="98af6-104">Contains information about a button that a File Manager extension DLL is adding to the toolbar of File Manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="98af6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98af6-105">Syntax</span></span>


```C++
typedef struct tagEXT_BUTTON {
  WORD idCommand;
  WORD idsHelp;
  WORD fsStyle;
} EXT_BUTTON, *LPEXT_BUTTON;
```



## <a name="members"></a><span data-ttu-id="98af6-106">Members</span><span class="sxs-lookup"><span data-stu-id="98af6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="98af6-107">**idCommand**</span><span class="sxs-lookup"><span data-stu-id="98af6-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="98af6-108">Tipo: **WORD**</span><span class="sxs-lookup"><span data-stu-id="98af6-108">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="98af6-109">Identificador de comando para el botón.</span><span class="sxs-lookup"><span data-stu-id="98af6-109">A command identifier for the button.</span></span>

</dd> <dt>

<span data-ttu-id="98af6-110">**idsHelp**</span><span class="sxs-lookup"><span data-stu-id="98af6-110">**idsHelp**</span></span>
</dt> <dd>

<span data-ttu-id="98af6-111">Tipo: **WORD**</span><span class="sxs-lookup"><span data-stu-id="98af6-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="98af6-112">Identificador de la cadena de Ayuda del botón.</span><span class="sxs-lookup"><span data-stu-id="98af6-112">The identifier of the Help string for the button.</span></span>

</dd> <dt>

<span data-ttu-id="98af6-113">**fsStyle**</span><span class="sxs-lookup"><span data-stu-id="98af6-113">**fsStyle**</span></span>
</dt> <dd>

<span data-ttu-id="98af6-114">Tipo: **WORD**</span><span class="sxs-lookup"><span data-stu-id="98af6-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="98af6-115">Estilo del botón.</span><span class="sxs-lookup"><span data-stu-id="98af6-115">The style of the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98af6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98af6-116">Requirements</span></span>



| <span data-ttu-id="98af6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="98af6-117">Requirement</span></span> | <span data-ttu-id="98af6-118">Value</span><span class="sxs-lookup"><span data-stu-id="98af6-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="98af6-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98af6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="98af6-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="98af6-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="98af6-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98af6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="98af6-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="98af6-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="98af6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98af6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="98af6-124"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="98af6-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98af6-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="98af6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98af6-126">**FMEVENT \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="98af6-126">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> <dt>

[<span data-ttu-id="98af6-127">**FMS \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="98af6-127">**FMS\_TOOLBARLOAD**</span></span>](fms-toolbarload.md)
</dt> </dl>

 

 




