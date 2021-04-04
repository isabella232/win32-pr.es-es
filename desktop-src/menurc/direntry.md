---
title: Estructura de direntary
description: Contiene un ordinal único que identifica una fuente individual en el grupo de recursos de fuentes. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: 4afc561e-bc98-4968-9a00-5002870b0c5e
keywords:
- Menús de la estructura de direntary y otros recursos
topic_type:
- apiref
api_name:
- DIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caed8f05a92abbeda39084b99b6806c2e28777a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802672"
---
# <a name="direntry-structure"></a><span data-ttu-id="08f7d-105">Estructura de direntary</span><span class="sxs-lookup"><span data-stu-id="08f7d-105">DIRENTRY structure</span></span>

<span data-ttu-id="08f7d-106">Contiene un ordinal único que identifica una fuente individual en el grupo de recursos de fuentes.</span><span class="sxs-lookup"><span data-stu-id="08f7d-106">Contains a unique ordinal that identifies an individual font in the font resource group.</span></span> <span data-ttu-id="08f7d-107">La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.</span><span class="sxs-lookup"><span data-stu-id="08f7d-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="08f7d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08f7d-108">Syntax</span></span>


```C++
typedef struct {
  WORD fontOrdinal;
} DIRENTRY;
```



## <a name="members"></a><span data-ttu-id="08f7d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="08f7d-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="08f7d-110">**fontOrdinal**</span><span class="sxs-lookup"><span data-stu-id="08f7d-110">**fontOrdinal**</span></span>
</dt> <dd>

<span data-ttu-id="08f7d-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="08f7d-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="08f7d-112">Identificador ordinal único para una fuente individual de un grupo de recursos de fuente.</span><span class="sxs-lookup"><span data-stu-id="08f7d-112">A unique ordinal identifier for an individual font in a font resource group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08f7d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08f7d-113">Remarks</span></span>

<span data-ttu-id="08f7d-114">La estructura [**FONTDIRENTRY**](fontdirentry.md) de la fuente especificada sigue directamente a **la estructura de la misma** .</span><span class="sxs-lookup"><span data-stu-id="08f7d-114">The [**FONTDIRENTRY**](fontdirentry.md) structure for the specified font directly follows the **DIRENTRY** structure for that font.</span></span>

## <a name="requirements"></a><span data-ttu-id="08f7d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08f7d-115">Requirements</span></span>



| <span data-ttu-id="08f7d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="08f7d-116">Requirement</span></span> | <span data-ttu-id="08f7d-117">Value</span><span class="sxs-lookup"><span data-stu-id="08f7d-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="08f7d-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08f7d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="08f7d-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="08f7d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="08f7d-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08f7d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="08f7d-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="08f7d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="08f7d-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="08f7d-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="08f7d-123">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="08f7d-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="08f7d-124">**FONTDIRENTRY**</span><span class="sxs-lookup"><span data-stu-id="08f7d-124">**FONTDIRENTRY**</span></span>](fontdirentry.md)
</dt> <dt>

[<span data-ttu-id="08f7d-125">**FONTGROUPHDR**</span><span class="sxs-lookup"><span data-stu-id="08f7d-125">**FONTGROUPHDR**</span></span>](fontgrouphdr.md)
</dt> <dt>

<span data-ttu-id="08f7d-126">**Vista**</span><span class="sxs-lookup"><span data-stu-id="08f7d-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="08f7d-127">Recursos</span><span class="sxs-lookup"><span data-stu-id="08f7d-127">Resources</span></span>](resources.md)
</dt> </dl>

 

 





