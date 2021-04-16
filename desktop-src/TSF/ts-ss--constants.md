---
title: Constantes de TS_SS_ (Textstor. h)
description: Las constantes de TS \_ SS \_ \, definidas antes del tiempo de ejecución en la estructura de estado de TS \_ , describen los Estados de documento estático.
ms.assetid: 17264527-946a-4648-a4eb-30db751602ab
topic_type:
- apiref
api_name:
- TS_SS_DISJOINTSEL
- TS_SS_REGIONS
- TS_SS_TRANSITORY
- TS_SS_NOHIDDENTEXT
- TS_SS_TKBAUTOCORRECTENABLE
- TS_SS_TKBPREDICTIONENABLE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773645b8a75b7e8eeafa40ed9fa95067743628d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685865"
---
# <a name="ts_ss_-constants"></a><span data-ttu-id="57c96-103">Constantes de TS \_ SS \_ \*</span><span class="sxs-lookup"><span data-stu-id="57c96-103">TS\_SS\_\* Constants</span></span>

<span data-ttu-id="57c96-104">Las constantes de TS \_ SS \_ \* , definidas antes del tiempo de ejecución en la estructura de [**\_ Estado de TS**](/windows/desktop/api/Textstor/ns-textstor-ts_status) , describen los Estados de documento estático.</span><span class="sxs-lookup"><span data-stu-id="57c96-104">The TS\_SS\_\* constants, defined before run time in the [**TS\_STATUS**](/windows/desktop/api/Textstor/ns-textstor-ts_status) structure, describe static document states.</span></span>



| <span data-ttu-id="57c96-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="57c96-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="57c96-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="57c96-106">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TS_SS_DISJOINTSEL"></span><span id="ts_ss_disjointsel"></span><dl> <span data-ttu-id="57c96-107"><dt>**TS \_ SS \_ DISJOINTSEL**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="57c96-107"><dt>**TS\_SS\_DISJOINTSEL**</dt> <dt>( 0x1 )</dt></span></span> </dl>                             | <span data-ttu-id="57c96-108">El documento admite selecciones múltiples.</span><span class="sxs-lookup"><span data-stu-id="57c96-108">The document supports multiple selections.</span></span><br/>                                                          |
| <span id="TS_SS_REGIONS"></span><span id="ts_ss_regions"></span><dl> <span data-ttu-id="57c96-109"><dt>**TS \_ \_Regiones de SS**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="57c96-109"><dt>**TS\_SS\_REGIONS**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                         | <span data-ttu-id="57c96-110">El documento puede contener varias regiones.</span><span class="sxs-lookup"><span data-stu-id="57c96-110">The document can contain multiple regions.</span></span><br/>                                                          |
| <span id="TS_SS_TRANSITORY"></span><span id="ts_ss_transitory"></span><dl> <span data-ttu-id="57c96-111"><dt>**TS \_ SS \_ transitorio**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="57c96-111"><dt>**TS\_SS\_TRANSITORY**</dt> <dt>( 0x4 )</dt></span></span> </dl>                                | <span data-ttu-id="57c96-112">Se espera que el documento tenga un ciclo de uso breve.</span><span class="sxs-lookup"><span data-stu-id="57c96-112">The document is expected to have a short usage cycle.</span></span><br/>                                               |
| <span id="TS_SS_NOHIDDENTEXT"></span><span id="ts_ss_nohiddentext"></span><dl> <span data-ttu-id="57c96-113"><dt>**TS \_ SS \_ NOHIDDENTEXT**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="57c96-113"><dt>**TS\_SS\_NOHIDDENTEXT**</dt> <dt>( 0x8 )</dt></span></span> </dl>                          | <span data-ttu-id="57c96-114">El documento nunca contendrá texto oculto.</span><span class="sxs-lookup"><span data-stu-id="57c96-114">The document will never contain hidden text.</span></span><br/>                                                        |
| <span id="TS_SS_TKBAUTOCORRECTENABLE"></span><span id="ts_ss_tkbautocorrectenable"></span><dl> <span data-ttu-id="57c96-115"><dt>**TS \_ SS \_ TKBAUTOCORRECTENABLE**</dt> <dt>(0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="57c96-115"><dt>**TS\_SS\_TKBAUTOCORRECTENABLE**</dt> <dt>( 0x10 )</dt></span></span> </dl> | <span data-ttu-id="57c96-116">**A partir de Windows 8:** El documento admite la corrección automática proporcionada por el teclado táctil.</span><span class="sxs-lookup"><span data-stu-id="57c96-116">**Starting with Windows 8:** The document supports autocorrection provided by the touch keyboard.</span></span><br/>   |
| <span id="TS_SS_TKBPREDICTIONENABLE"></span><span id="ts_ss_tkbpredictionenable"></span><dl> <span data-ttu-id="57c96-117"><dt>**TS \_ SS \_ TKBPREDICTIONENABLE**</dt> <dt>(0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="57c96-117"><dt>**TS\_SS\_TKBPREDICTIONENABLE**</dt> <dt>( 0x20 )</dt></span></span> </dl>    | <span data-ttu-id="57c96-118">**A partir de Windows 8:** El documento admite las sugerencias de texto que proporciona el teclado táctil.</span><span class="sxs-lookup"><span data-stu-id="57c96-118">**Starting with Windows 8:** The document supports text suggestions provided by the touch keyboard.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="57c96-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57c96-119">Remarks</span></span>

<span data-ttu-id="57c96-120">El miembro **dwStaticFlags** de la estructura de **\_ Estado de TS** utiliza estas constantes.</span><span class="sxs-lookup"><span data-stu-id="57c96-120">The **dwStaticFlags** member of the **TS\_STATUS** structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="57c96-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57c96-121">Requirements</span></span>



| <span data-ttu-id="57c96-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="57c96-122">Requirement</span></span> | <span data-ttu-id="57c96-123">Value</span><span class="sxs-lookup"><span data-stu-id="57c96-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57c96-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57c96-124">Minimum supported client</span></span><br/> | <span data-ttu-id="57c96-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="57c96-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="57c96-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57c96-126">Minimum supported server</span></span><br/> | <span data-ttu-id="57c96-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="57c96-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="57c96-128">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="57c96-128">Redistributable</span></span><br/>          | <span data-ttu-id="57c96-129">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="57c96-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="57c96-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57c96-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="57c96-131"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="57c96-131"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="57c96-132">IDL</span><span class="sxs-lookup"><span data-stu-id="57c96-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="57c96-133"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="57c96-133"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57c96-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="57c96-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57c96-135">**Estado de TS \_**</span><span class="sxs-lookup"><span data-stu-id="57c96-135">**TS\_STATUS**</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

<span data-ttu-id="57c96-136">[**Estado de TF \_**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="57c96-136">[**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> </dl>

 

