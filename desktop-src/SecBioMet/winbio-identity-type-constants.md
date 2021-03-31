---
title: Constantes de WINBIO_IDENTITY_TYPE (Winbio \_ Types. h)
description: Especifique el formato de la información de identidad contenida en la estructura de identidad de WINBIO \_ .
ms.assetid: 27A01538-9B26-4A29-8ADB-ED9C5D5808B3
topic_type:
- apiref
api_name:
- WINBIO_ID_TYPE_NULL
- WINBIO_ID_TYPE_WILDCARD
- WINBIO_ID_TYPE_GUID
- WINBIO_ID_TYPE_SID
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dad068c6838f0a3a675970b7c9359b12ea8faa2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996165"
---
# <a name="winbio_identity_type-constants"></a><span data-ttu-id="c451e-103">Constantes de tipo de \_ identidad WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="c451e-103">WINBIO\_IDENTITY\_TYPE Constants</span></span>

<span data-ttu-id="c451e-104">Las constantes **de \_ \_ tipo de identidad WINBIO** siguientes se pueden usar para especificar el formato de la información de identidad contenida en la estructura de [**\_ identidad de WINBIO**](winbio-identity.md) .</span><span class="sxs-lookup"><span data-stu-id="c451e-104">The following **WINBIO\_IDENTITY\_TYPE** constants can be used to specify the format of the identity information contained in the [**WINBIO\_IDENTITY**](winbio-identity.md) structure.</span></span>



| <span data-ttu-id="c451e-105">Constante</span><span class="sxs-lookup"><span data-stu-id="c451e-105">Constant</span></span>                                                                                                                                                                                      | <span data-ttu-id="c451e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="c451e-106">Description</span></span>                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <span data-ttu-id="c451e-107"><dt>**WINBIO \_ ID \_ Type \_ null**</dt></span><span class="sxs-lookup"><span data-stu-id="c451e-107"><dt>**WINBIO\_ID\_TYPE\_NULL**</dt></span></span> </dl>             | <span data-ttu-id="c451e-108">La plantilla no tiene ningún identificador asociado.</span><span class="sxs-lookup"><span data-stu-id="c451e-108">The template has no associated ID.</span></span> <br/>            |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <span data-ttu-id="c451e-109"><dt>**\_ \_ carácter comodín de tipo de identificador WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c451e-109"><dt>**WINBIO\_ID\_TYPE\_WILDCARD**</dt></span></span> </dl> | <span data-ttu-id="c451e-110">La estructura coincide con todas las identidades de plantilla.</span><span class="sxs-lookup"><span data-stu-id="c451e-110">The structure matches all template identities.</span></span><br/> |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <span data-ttu-id="c451e-111"><dt>**\_GUID de \_ tipo de identificador WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c451e-111"><dt>**WINBIO\_ID\_TYPE\_GUID**</dt></span></span> </dl>             | <span data-ttu-id="c451e-112">Un GUID identifica la plantilla.</span><span class="sxs-lookup"><span data-stu-id="c451e-112">A GUID identifies the template.</span></span><br/>                |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <span data-ttu-id="c451e-113"><dt>**identificador de WINBIO de \_ tipo ID. \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c451e-113"><dt>**WINBIO\_ID\_TYPE\_SID**</dt></span></span> </dl>                | <span data-ttu-id="c451e-114">Un SID de cuenta identifica la plantilla.</span><span class="sxs-lookup"><span data-stu-id="c451e-114">An account SID identifies the template.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="c451e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c451e-115">Requirements</span></span>



| <span data-ttu-id="c451e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c451e-116">Requirement</span></span> | <span data-ttu-id="c451e-117">Value</span><span class="sxs-lookup"><span data-stu-id="c451e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c451e-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c451e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c451e-119">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c451e-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="c451e-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c451e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c451e-121">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c451e-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c451e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c451e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c451e-123"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c451e-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c451e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c451e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c451e-125">Constantes de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="c451e-125">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="c451e-126">**identidad de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="c451e-126">**WINBIO\_IDENTITY**</span></span>](winbio-identity.md)
</dt> </dl>

 

 





