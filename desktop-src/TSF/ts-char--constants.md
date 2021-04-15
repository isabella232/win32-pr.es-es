---
title: Constantes de TS_CHAR_ (Textstor. h)
description: Las \_ constantes char \_ \ de TS describen el tipo de carácter.
ms.assetid: b40ca931-d45c-4101-9380-bb2b3ad25fba
topic_type:
- apiref
api_name:
- TS_CHAR_EMBEDDED
- TS_CHAR_REGION
- TS_CHAR_REPLACEMENT
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25f66006dcb37e2504785b2b28ca1f328edfcfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422169"
---
# <a name="ts_char_-constants"></a><span data-ttu-id="df2a9-103">\_Constantes de caracteres de TS \_ \*</span><span class="sxs-lookup"><span data-stu-id="df2a9-103">TS\_CHAR\_\* Constants</span></span>

<span data-ttu-id="df2a9-104">Las constantes de caracteres de TS \_ \_ \* describen el tipo de carácter.</span><span class="sxs-lookup"><span data-stu-id="df2a9-104">The TS\_CHAR\_\* constants describe the type of character.</span></span>



| <span data-ttu-id="df2a9-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="df2a9-105">Constant/value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="df2a9-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="df2a9-106">Description</span></span>                                                                                         |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| <span id="TS_CHAR_EMBEDDED"></span><span id="ts_char_embedded"></span><dl> <span data-ttu-id="df2a9-107"><dt>**TS \_ CARÁCTER \_ incrustado**</dt> <dt>(0xfffc)</dt></span><span class="sxs-lookup"><span data-stu-id="df2a9-107"><dt>**TS\_CHAR\_EMBEDDED**</dt> <dt>( 0xfffc )</dt></span></span> </dl>          | <span data-ttu-id="df2a9-108">El carácter es un carácter de reemplazo de objeto Unicode 2,1.</span><span class="sxs-lookup"><span data-stu-id="df2a9-108">The character is a Unicode 2.1 object-replacement character.</span></span><br/>                             |
| <span id="TS_CHAR_REGION"></span><span id="ts_char_region"></span><dl> <span data-ttu-id="df2a9-109"><dt>**TS \_ \_Región char**</dt> <dt>(0)</dt></span><span class="sxs-lookup"><span data-stu-id="df2a9-109"><dt>**TS\_CHAR\_REGION**</dt> <dt>( 0 )</dt></span></span> </dl>                     | <span data-ttu-id="df2a9-110">El carácter es un límite de región.</span><span class="sxs-lookup"><span data-stu-id="df2a9-110">The character is a region boundary.</span></span><br/>                                                      |
| <span id="TS_CHAR_REPLACEMENT"></span><span id="ts_char_replacement"></span><dl> <span data-ttu-id="df2a9-111"><dt>**TS \_ \_Reemplazo de char**</dt> <dt>(0xfffd)</dt></span><span class="sxs-lookup"><span data-stu-id="df2a9-111"><dt>**TS\_CHAR\_REPLACEMENT**</dt> <dt>( 0xfffd )</dt></span></span> </dl> | <span data-ttu-id="df2a9-112">El carácter es un carácter de marcador de posición de texto oculto o un carácter de reemplazo Unicode.</span><span class="sxs-lookup"><span data-stu-id="df2a9-112">The character is a hidden-text placeholder character or a Unicode replacement character.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="df2a9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df2a9-113">Requirements</span></span>



| <span data-ttu-id="df2a9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="df2a9-114">Requirement</span></span> | <span data-ttu-id="df2a9-115">Value</span><span class="sxs-lookup"><span data-stu-id="df2a9-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df2a9-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df2a9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="df2a9-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="df2a9-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="df2a9-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df2a9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="df2a9-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="df2a9-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="df2a9-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="df2a9-120">Redistributable</span></span><br/>          | <span data-ttu-id="df2a9-121">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="df2a9-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="df2a9-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df2a9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="df2a9-123"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="df2a9-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="df2a9-124">IDL</span><span class="sxs-lookup"><span data-stu-id="df2a9-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="df2a9-125"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="df2a9-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df2a9-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="df2a9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df2a9-127">Objetos incrustados</span><span class="sxs-lookup"><span data-stu-id="df2a9-127">Embedded Objects</span></span>](embedded-objects.md)
</dt> </dl>

 

 





