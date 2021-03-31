---
title: Constantes de WINBIO_BIR_QUALITY (Winbio \_ Types. h)
description: Especifique la calidad relativa de los datos biométricos en el BIR si no se ha especificado un valor entero de 0 a 100.
ms.assetid: A42AA21B-9AA5-4DB6-B58F-0776BEC63E6C
topic_type:
- apiref
api_name:
- WINBIO_DATA_QUALITY_NOT_SET
- WINBIO_DATA_QUALITY_NOT_SUPPORTED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1eb0881672c9e3bf51214cff93cb3f68d802b04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151123"
---
# <a name="winbio_bir_quality-constants"></a><span data-ttu-id="ece2f-103">Constantes de calidad de WINBIO \_ Bir \_</span><span class="sxs-lookup"><span data-stu-id="ece2f-103">WINBIO\_BIR\_QUALITY Constants</span></span>

<span data-ttu-id="ece2f-104">El miembro de **calidad** de datos de la estructura de [**\_ \_ encabezado WINBIO Bir**](winbio-bir-header.md) utiliza las marcas siguientes para especificar la calidad relativa de los datos biométricos en Bir si no se ha especificado un valor entero de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="ece2f-104">The following flags are used by the **DataQuality** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure to specify the relative quality of biometric data in the BIR if an integer value from 0 to 100 has not been specified.</span></span>



| <span data-ttu-id="ece2f-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="ece2f-105">Constant/value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="ece2f-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="ece2f-106">Description</span></span>                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <span data-ttu-id="ece2f-107"><dt>**WINBIO \_ Calidad de datos \_ \_ no \_ establecida**</dt> <dt> 1</dt></span><span class="sxs-lookup"><span data-stu-id="ece2f-107"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SET**</dt> <dt> 1</dt></span></span> </dl>                   | <span data-ttu-id="ece2f-108">El creador de BIR admite las medidas de calidad, pero no se establece ningún valor en BIR.</span><span class="sxs-lookup"><span data-stu-id="ece2f-108">Quality measurements are supported by the BIR creator, but no value is set in the BIR.</span></span><br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <span data-ttu-id="ece2f-109"><dt>**WINBIO \_ Calidad de datos \_ \_ no \_ admitida**</dt> <dt> 2</dt></span><span class="sxs-lookup"><span data-stu-id="ece2f-109"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SUPPORTED**</dt> <dt> 2</dt></span></span> </dl> | <span data-ttu-id="ece2f-110">El creador de BIR no admite las medidas de calidad.</span><span class="sxs-lookup"><span data-stu-id="ece2f-110">Quality measurements are not supported by the BIR creator.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="ece2f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ece2f-111">Requirements</span></span>



| <span data-ttu-id="ece2f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ece2f-112">Requirement</span></span> | <span data-ttu-id="ece2f-113">Value</span><span class="sxs-lookup"><span data-stu-id="ece2f-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece2f-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ece2f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ece2f-115">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ece2f-115">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="ece2f-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ece2f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ece2f-117">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ece2f-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ece2f-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ece2f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ece2f-119"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ece2f-119"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ece2f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="ece2f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ece2f-121">Constantes de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="ece2f-121">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





