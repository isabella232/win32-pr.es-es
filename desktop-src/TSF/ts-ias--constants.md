---
title: Constantes de TS_IAS_ (Textstor. h)
description: Las constantes de IAS de TS \_ \_ se usan como marcas de bits para controlar la inserción de texto o de objetos incrustados en una selección o un punto de inserción.
ms.assetid: 58e0d13c-d90c-41d2-bd93-4eba5fe0a69a
topic_type:
- apiref
api_name:
- TS_IAS_NOQUERY
- TS_IAS_QUERYONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d59584295567c586ebd8db7e5f63366fd8272f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150331"
---
# <a name="ts_ias_-constants"></a><span data-ttu-id="249ba-103">\_Constantes de IAS de TS \_ \*</span><span class="sxs-lookup"><span data-stu-id="249ba-103">TS\_IAS\_\* Constants</span></span>

<span data-ttu-id="249ba-104">Las \_ constantes de IAS \_ \* de TS se utilizan como marcas de bits para controlar la inserción de texto o de objetos incrustados en una selección o un punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="249ba-104">The TS\_IAS\_\* constants are used as bitfield flags to control insertion of text or embedded objects at a selection or insertion point.</span></span>



| <span data-ttu-id="249ba-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="249ba-105">Constant/value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="249ba-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="249ba-106">Description</span></span>                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IAS_NOQUERY"></span><span id="ts_ias_noquery"></span><dl> <span data-ttu-id="249ba-107"><dt>**TS \_ \_NOquery de IAS**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="249ba-107"><dt>**TS\_IAS\_NOQUERY**</dt> <dt>( 0x1 )</dt></span></span> </dl>       | <span data-ttu-id="249ba-108">Se inserta texto y el puntero de intervalo se establece en **null** al salir.</span><span class="sxs-lookup"><span data-stu-id="249ba-108">Text is inserted and the range pointer is set to **NULL** upon exit.</span></span> <span data-ttu-id="249ba-109">No se puede combinar con la \_ marca QUERYONLY de IAS de TS \_ .</span><span class="sxs-lookup"><span data-stu-id="249ba-109">Cannot be combined with the TS\_IAS\_QUERYONLY flag.</span></span><br/>          |
| <span id="TS_IAS_QUERYONLY"></span><span id="ts_ias_queryonly"></span><dl> <span data-ttu-id="249ba-110"><dt>**TS \_ \_QUERYONLY IAS**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="249ba-110"><dt>**TS\_IAS\_QUERYONLY**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="249ba-111">No realice la inserción.</span><span class="sxs-lookup"><span data-stu-id="249ba-111">Do not perform the insertion.</span></span> <span data-ttu-id="249ba-112">El autor de la llamada solo requiere que se establezca el puntero de intervalo.</span><span class="sxs-lookup"><span data-stu-id="249ba-112">Caller only requires the range pointer to be set.</span></span> <span data-ttu-id="249ba-113">No se puede combinar con la \_ marca NOquery de IAS de TS \_ .</span><span class="sxs-lookup"><span data-stu-id="249ba-113">Cannot be combined with the TS\_IAS\_NOQUERY flag.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="249ba-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="249ba-114">Requirements</span></span>



| <span data-ttu-id="249ba-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="249ba-115">Requirement</span></span> | <span data-ttu-id="249ba-116">Value</span><span class="sxs-lookup"><span data-stu-id="249ba-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="249ba-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="249ba-117">Minimum supported client</span></span><br/> | <span data-ttu-id="249ba-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="249ba-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="249ba-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="249ba-119">Minimum supported server</span></span><br/> | <span data-ttu-id="249ba-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="249ba-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="249ba-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="249ba-121">Redistributable</span></span><br/>          | <span data-ttu-id="249ba-122">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="249ba-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="249ba-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="249ba-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="249ba-124"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="249ba-124"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="249ba-125">IDL</span><span class="sxs-lookup"><span data-stu-id="249ba-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="249ba-126"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="249ba-126"><dt>Textstor.idl</dt></span></span> </dl> |



 

 





