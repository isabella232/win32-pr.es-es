---
title: Constantes de TS_SD_ (Textstor. h)
description: Las constantes de TS \_ SD \_ \ describen los Estados de documentos dinámicos usados por una aplicación en tiempo de ejecución.
ms.assetid: fb673e42-bee7-484e-872a-d709d5ca12f2
topic_type:
- apiref
api_name:
- TS_SD_READONLY
- TS_SD_LOADING
- TS_SD_MASKALL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565bc97b9fa2d1474f1ba36cd8137e63125541e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685948"
---
# <a name="ts_sd_-constants"></a><span data-ttu-id="30339-103">Constantes de TS \_ SD \_ \*</span><span class="sxs-lookup"><span data-stu-id="30339-103">TS\_SD\_\* Constants</span></span>

<span data-ttu-id="30339-104">Las constantes de TS \_ SD \_ \* describen los Estados de documentos dinámicos usados por una aplicación en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="30339-104">The TS\_SD\_\* constants describe dynamic document states used by an application at runtime.</span></span>



| <span data-ttu-id="30339-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="30339-105">Constant/value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="30339-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="30339-106">Description</span></span>                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TS_SD_READONLY"></span><span id="ts_sd_readonly"></span><dl> <span data-ttu-id="30339-107"><dt>**TS \_ SD \_ ReadOnly**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="30339-107"><dt>**TS\_SD\_READONLY**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="30339-108">El documento es de solo lectura y no se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="30339-108">The document is read-only and cannot be modified.</span></span><br/> |
| <span id="TS_SD_LOADING"></span><span id="ts_sd_loading"></span><dl> <span data-ttu-id="30339-109"><dt>**TS \_ \_Carga de SD**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="30339-109"><dt>**TS\_SD\_LOADING**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                 | <span data-ttu-id="30339-110">El documento se está cargando y podría estar incompleto.</span><span class="sxs-lookup"><span data-stu-id="30339-110">The document is loading and might be incomplete.</span></span><br/>  |
| <span id="TS_SD_MASKALL"></span><span id="ts_sd_maskall"></span><dl> <span data-ttu-id="30339-111"><dt>**TS \_ SD \_ MASKALL**</dt> <dt>(TS \_ SD \_ ReadOnly \| TS \_ SD \_ loading)</dt></span><span class="sxs-lookup"><span data-stu-id="30339-111"><dt>**TS\_SD\_MASKALL**</dt> <dt>( TS\_SD\_READONLY \| TS\_SD\_LOADING )</dt></span></span> </dl> | <span data-ttu-id="30339-112">El documento es tanto de solo lectura como de carga.</span><span class="sxs-lookup"><span data-stu-id="30339-112">The document is both read-only and loading.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="30339-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30339-113">Remarks</span></span>

<span data-ttu-id="30339-114">El miembro **dwDynamicFlags** de la estructura de [ \_ Estado de TS](/windows/desktop/api/Textstor/ns-textstor-ts_status) utiliza estas constantes.</span><span class="sxs-lookup"><span data-stu-id="30339-114">The **dwDynamicFlags** member of the [TS\_STATUS](/windows/desktop/api/Textstor/ns-textstor-ts_status) structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="30339-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30339-115">Requirements</span></span>



| <span data-ttu-id="30339-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="30339-116">Requirement</span></span> | <span data-ttu-id="30339-117">Value</span><span class="sxs-lookup"><span data-stu-id="30339-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30339-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30339-118">Minimum supported client</span></span><br/> | <span data-ttu-id="30339-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="30339-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="30339-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30339-120">Minimum supported server</span></span><br/> | <span data-ttu-id="30339-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="30339-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="30339-122">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="30339-122">Redistributable</span></span><br/>          | <span data-ttu-id="30339-123">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="30339-123">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="30339-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30339-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="30339-125"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="30339-125"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="30339-126">IDL</span><span class="sxs-lookup"><span data-stu-id="30339-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="30339-127"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="30339-127"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30339-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="30339-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30339-129">Estado de TS \_</span><span class="sxs-lookup"><span data-stu-id="30339-129">TS\_STATUS</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[<span data-ttu-id="30339-130">Constantes de TF \_ SD \_ \*</span><span class="sxs-lookup"><span data-stu-id="30339-130">TF\_SD\_\* Constants</span></span>](tf-sd--constants.md)
</dt> </dl>

 

 





