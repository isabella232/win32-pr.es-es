---
title: Estructura de DSA_SEC_PAGE_INFO
description: Se usa con la \_ hoja de ADSPROP de WM \_ \_ creación y la \_ hoja DSA de WM creación de mensajes de \_ \_ \_ notificación para definir una hoja de propiedades secundaria en un complemento de MMC de Active Directory.
ms.assetid: 422d84dc-6b5e-43bf-ac4f-3b99cb59f9df
ms.tgt_platform: multiple
keywords:
- Estructura de DSA_SEC_PAGE_INFO Active Directory
- PDSA_SEC_PAGE_INFO puntero de estructura Active Directory
topic_type:
- apiref
api_name:
- DSA_SEC_PAGE_INFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e4c8602a958c50c72942d89657a812d24f64571d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996656"
---
# <a name="dsa_sec_page_info-structure"></a><span data-ttu-id="d9098-105">\_Estructura de \_ información de página DSA s \_</span><span class="sxs-lookup"><span data-stu-id="d9098-105">DSA\_SEC\_PAGE\_INFO structure</span></span>

<span data-ttu-id="d9098-106">La estructura de información de la **\_ \_ página \_ DSA sec** se usa con la hoja de [**ADSPROP de WM \_ \_ \_ creación**](wm-adsprop-sheet-create.md) y la hoja de DSA de WM creación de mensajes de [**\_ \_ \_ \_ notificación**](wm-dsa-sheet-create-notify.md) para definir una hoja de propiedades secundaria en un complemento MMC de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d9098-106">The **DSA\_SEC\_PAGE\_INFO** structure is used with the [**WM\_ADSPROP\_SHEET\_CREATE**](wm-adsprop-sheet-create.md) and [**WM\_DSA\_SHEET\_CREATE\_NOTIFY**](wm-dsa-sheet-create-notify.md) messages to define a secondary property sheet in an Active Directory MMC snap-in.</span></span>

> [!Note]  
> <span data-ttu-id="d9098-107">Esta estructura no está definida en un archivo de encabezado publicado.</span><span class="sxs-lookup"><span data-stu-id="d9098-107">This structure is not defined in a published header file.</span></span> <span data-ttu-id="d9098-108">Para usar esta estructura, debe definirla en el formato exacto que se muestra.</span><span class="sxs-lookup"><span data-stu-id="d9098-108">To use this structure, define it in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d9098-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9098-109">Syntax</span></span>


```C++
typedef struct _DSA_SEC_PAGE_INFO {
  HWND          hwndParentSheet;
  DWORD         offsetTitle;
  DSOBJECTNAMES dsObjectNames;
} DSA_SEC_PAGE_INFO, *PDSA_SEC_PAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="d9098-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="d9098-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="d9098-111">**hwndParentSheet**</span><span class="sxs-lookup"><span data-stu-id="d9098-111">**hwndParentSheet**</span></span>
</dt> <dd>

<span data-ttu-id="d9098-112">Contiene el identificador de ventana del elemento primario de la hoja de propiedades secundaria.</span><span class="sxs-lookup"><span data-stu-id="d9098-112">Contains the window handle of the parent of the secondary property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="d9098-113">**offsetTitle**</span><span class="sxs-lookup"><span data-stu-id="d9098-113">**offsetTitle**</span></span>
</dt> <dd>

<span data-ttu-id="d9098-114">Contiene el desplazamiento, en bytes, desde el inicio de la estructura de **\_ información de \_ página \_ de DSA s** hasta una cadena Unicode terminada en null que contiene el título de la hoja de propiedades secundaria.</span><span class="sxs-lookup"><span data-stu-id="d9098-114">Contains the offset, in bytes, from the start of the **DSA\_SEC\_PAGE\_INFO** structure to a NULL-terminated, Unicode string that contains the title of the secondary property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="d9098-115">**dsObjectNames**</span><span class="sxs-lookup"><span data-stu-id="d9098-115">**dsObjectNames**</span></span>
</dt> <dd>

<span data-ttu-id="d9098-116">Contiene una estructura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) que define la hoja de propiedades secundaria.</span><span class="sxs-lookup"><span data-stu-id="d9098-116">Contains a [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) structure that defines the secondary property sheet.</span></span> <span data-ttu-id="d9098-117">Solo se puede crear una hoja de propiedades secundaria a la vez, por lo que la estructura **DSOBJECTNAMES** solo puede contener una estructura [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .</span><span class="sxs-lookup"><span data-stu-id="d9098-117">Only one secondary property sheet can be created at a time, so the **DSOBJECTNAMES** structure can only contain one [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d9098-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9098-118">Requirements</span></span>



| <span data-ttu-id="d9098-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9098-119">Requirement</span></span> | <span data-ttu-id="d9098-120">Value</span><span class="sxs-lookup"><span data-stu-id="d9098-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d9098-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9098-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d9098-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9098-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d9098-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9098-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d9098-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9098-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9098-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9098-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9098-126">**hoja de ADSPROP de WM \_ \_ \_ creación**</span><span class="sxs-lookup"><span data-stu-id="d9098-126">**WM\_ADSPROP\_SHEET\_CREATE**</span></span>](wm-adsprop-sheet-create.md)
</dt> <dt>

[<span data-ttu-id="d9098-127">**\_ \_ \_ crear notificación de la hoja DSA de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d9098-127">**WM\_DSA\_SHEET\_CREATE\_NOTIFY**</span></span>](wm-dsa-sheet-create-notify.md)
</dt> <dt>

[<span data-ttu-id="d9098-128">**DSOBJECTNAMES**</span><span class="sxs-lookup"><span data-stu-id="d9098-128">**DSOBJECTNAMES**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[<span data-ttu-id="d9098-129">**DSOBJECT**</span><span class="sxs-lookup"><span data-stu-id="d9098-129">**DSOBJECT**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> </dl>

 

 





