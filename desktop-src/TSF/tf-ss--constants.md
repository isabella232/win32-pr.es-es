---
title: Constantes de TF_SS_ (msctf. h)
description: Las constantes de TF \_ SS \_ \, definidas antes del tiempo de ejecución en la estructura de estado de TF \_ , describen los Estados de documento estático.
ms.assetid: 371aeeda-f081-4506-ba51-79c6a8bc8768
topic_type:
- apiref
api_name:
- TF_SS_DISJOINTSEL
- TF_SS_REGIONS
- TF_SS_TRANSITORY
- TF_SS_TKBAUTOCORRECTENABLE
- TF_SS_TKBPREDICTIONENABLE
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1028b78e74ed10c572feb904baa8ec395087ee3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079476"
---
# <a name="tf_ss_-constants"></a><span data-ttu-id="8b9bb-103">Constantes de TF \_ SS \_ \*</span><span class="sxs-lookup"><span data-stu-id="8b9bb-103">TF\_SS\_\* Constants</span></span>

<span data-ttu-id="8b9bb-104">Las constantes de TF \_ SS \_ \* , definidas antes del tiempo de ejecución en la estructura de [**\_ Estado de TF**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) , describen los Estados de documento estático.</span><span class="sxs-lookup"><span data-stu-id="8b9bb-104">The TF\_SS\_\* constants, defined before run time in the [**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) structure, describe static document states.</span></span>



| <span data-ttu-id="8b9bb-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="8b9bb-105">Constant/value</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="8b9bb-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b9bb-106">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TF_SS_DISJOINTSEL"></span><span id="tf_ss_disjointsel"></span><dl> <span data-ttu-id="8b9bb-107"><dt>**TF \_ SS \_ DISJOINTSEL**</dt> <dt>(TS \_ SS \_ DISJOINTSEL)</dt></span><span class="sxs-lookup"><span data-stu-id="8b9bb-107"><dt>**TF\_SS\_DISJOINTSEL**</dt> <dt>( TS\_SS\_DISJOINTSEL )</dt></span></span> </dl>                                     | <span data-ttu-id="8b9bb-108">El documento admite selecciones múltiples.</span><span class="sxs-lookup"><span data-stu-id="8b9bb-108">The document supports multiple selections.</span></span><br/>                                                          |
| <span id="TF_SS_REGIONS"></span><span id="tf_ss_regions"></span><dl> <span data-ttu-id="8b9bb-109"><dt>**TF \_ \_regiones de SS**</dt> <dt>(regiones de TS \_ SS \_ )</dt></span><span class="sxs-lookup"><span data-stu-id="8b9bb-109"><dt>**TF\_SS\_REGIONS**</dt> <dt>( TS\_SS\_REGIONS )</dt></span></span> </dl>                                                     | <span data-ttu-id="8b9bb-110">El documento puede contener varias regiones.</span><span class="sxs-lookup"><span data-stu-id="8b9bb-110">The document can contain multiple regions.</span></span><br/>                                                          |
| <span id="TF_SS_TRANSITORY"></span><span id="tf_ss_transitory"></span><dl> <span data-ttu-id="8b9bb-111"><dt>**TF \_ SS \_ transitorio**</dt> <dt>(TS \_ SS \_ transitorio)</dt></span><span class="sxs-lookup"><span data-stu-id="8b9bb-111"><dt>**TF\_SS\_TRANSITORY**</dt> <dt>( TS\_SS\_TRANSITORY )</dt></span></span> </dl>                                         | <span data-ttu-id="8b9bb-112">Se espera que el documento tenga un ciclo de uso breve.</span><span class="sxs-lookup"><span data-stu-id="8b9bb-112">The document is expected to have a short usage cycle.</span></span><br/>                                               |
| <span id="TF_SS_TKBAUTOCORRECTENABLE"></span><span id="tf_ss_tkbautocorrectenable"></span><dl> <span data-ttu-id="8b9bb-113"><dt>**TF \_ SS \_ TKBAUTOCORRECTENABLE**</dt> <dt>(TS \_ SS \_ TKBAUTOCORRECTENABLE)</dt></span><span class="sxs-lookup"><span data-stu-id="8b9bb-113"><dt>**TF\_SS\_TKBAUTOCORRECTENABLE**</dt> <dt>( TS\_SS\_TKBAUTOCORRECTENABLE )</dt></span></span> </dl> | <span data-ttu-id="8b9bb-114">**A partir de Windows 8:** El documento admite la corrección automática proporcionada por el teclado táctil.</span><span class="sxs-lookup"><span data-stu-id="8b9bb-114">**Starting with Windows 8:** The document supports autocorrection provided by the touch keyboard.</span></span><br/>   |
| <span id="TF_SS_TKBPREDICTIONENABLE"></span><span id="tf_ss_tkbpredictionenable"></span><dl> <span data-ttu-id="8b9bb-115"><dt>**TF \_ SS \_ TKBPREDICTIONENABLE**</dt> <dt>(TS \_ SS \_ TKBPREDICTIONENABLE)</dt></span><span class="sxs-lookup"><span data-stu-id="8b9bb-115"><dt>**TF\_SS\_TKBPREDICTIONENABLE**</dt> <dt>( TS\_SS\_TKBPREDICTIONENABLE )</dt></span></span> </dl>     | <span data-ttu-id="8b9bb-116">**A partir de Windows 8:** El documento admite las sugerencias de texto que proporciona el teclado táctil.</span><span class="sxs-lookup"><span data-stu-id="8b9bb-116">**Starting with Windows 8:** The document supports text suggestions provided by the touch keyboard.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8b9bb-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b9bb-117">Remarks</span></span>

<span data-ttu-id="8b9bb-118">El miembro **dwStaticFlags** de la estructura de estado de TF \_ utiliza estas constantes.</span><span class="sxs-lookup"><span data-stu-id="8b9bb-118">The **dwStaticFlags** member of the TF\_STATUS structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b9bb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b9bb-119">Requirements</span></span>



| <span data-ttu-id="8b9bb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b9bb-120">Requirement</span></span> | <span data-ttu-id="8b9bb-121">Value</span><span class="sxs-lookup"><span data-stu-id="8b9bb-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8b9bb-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b9bb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8b9bb-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8b9bb-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8b9bb-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b9bb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8b9bb-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8b9bb-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8b9bb-126">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="8b9bb-126">Redistributable</span></span><br/>          | <span data-ttu-id="8b9bb-127">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8b9bb-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="8b9bb-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b9bb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b9bb-129"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b9bb-129"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b9bb-130">IDL</span><span class="sxs-lookup"><span data-stu-id="8b9bb-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8b9bb-131"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8b9bb-131"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b9bb-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b9bb-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="8b9bb-133">[**Estado de TF \_**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8b9bb-133">[**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> </dl>

 

