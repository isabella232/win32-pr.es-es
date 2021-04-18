---
title: Estructura MENUHELPID
description: Contiene los datos finales escritos en el \_ recurso de menú RT para un menú o un submenú si el miembro resInfo de la estructura POPUPMENUITEM se establece en MFR \_ Popup.
ms.assetid: f17fdaaa-b37c-4902-bad4-a1181ffee9f9
keywords:
- Menús de la estructura MENUHELPID y otros recursos
topic_type:
- apiref
api_name:
- MENUHELPID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b90b5a4745433c92a859a168611aa1c14f1fa45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666073"
---
# <a name="menuhelpid-structure"></a><span data-ttu-id="222ee-104">Estructura MENUHELPID</span><span class="sxs-lookup"><span data-stu-id="222ee-104">MENUHELPID structure</span></span>

<span data-ttu-id="222ee-105">Contiene los datos finales escritos en el recurso de [**\_ menú RT**](/windows/desktop/menurc/resource-types) para un menú o un submenú si el miembro **ResInfo** de la estructura [**POPUPMENUITEM**](popupmenuitem.md) se establece en **MFR \_ popup**.</span><span class="sxs-lookup"><span data-stu-id="222ee-105">Contains the final data written to the [**RT\_MENU**](/windows/desktop/menurc/resource-types) resource for a menu or submenu if the **resInfo** member of the [**POPUPMENUITEM**](popupmenuitem.md) structure is set to **MFR\_POPUP**.</span></span> <span data-ttu-id="222ee-106">La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.</span><span class="sxs-lookup"><span data-stu-id="222ee-106">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="222ee-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="222ee-107">Syntax</span></span>


```C++
typedef struct {
  DWORD helpID;
} MENUHELPID;
```



## <a name="members"></a><span data-ttu-id="222ee-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="222ee-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="222ee-109">**helpID**</span><span class="sxs-lookup"><span data-stu-id="222ee-109">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="222ee-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="222ee-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="222ee-111">El identificador que se usa para identificar el menú durante el procesamiento de la [**\_ ayuda de WM**](/windows/desktop/shell/wm-help) .</span><span class="sxs-lookup"><span data-stu-id="222ee-111">The identifier used to identify the menu during [**WM\_HELP**](/windows/desktop/shell/wm-help) processing.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="222ee-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="222ee-112">Requirements</span></span>



| <span data-ttu-id="222ee-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="222ee-113">Requirement</span></span> | <span data-ttu-id="222ee-114">Value</span><span class="sxs-lookup"><span data-stu-id="222ee-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="222ee-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="222ee-115">Minimum supported client</span></span><br/> | <span data-ttu-id="222ee-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="222ee-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="222ee-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="222ee-117">Minimum supported server</span></span><br/> | <span data-ttu-id="222ee-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="222ee-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="222ee-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="222ee-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="222ee-120">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="222ee-120">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="222ee-121">**MENUHEADER**</span><span class="sxs-lookup"><span data-stu-id="222ee-121">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="222ee-122">**POPUPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="222ee-122">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="222ee-123">**Vista**</span><span class="sxs-lookup"><span data-stu-id="222ee-123">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="222ee-124">Recursos</span><span class="sxs-lookup"><span data-stu-id="222ee-124">Resources</span></span>](resources.md)
</dt> </dl>

 

