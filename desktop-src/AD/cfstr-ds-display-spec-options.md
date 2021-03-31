---
title: CFSTR_DS_DISPLAY_SPEC_OPTIONS (DSClient. h)
description: El \_ formato del \_ \_ portapapeles CFSTR DS display Spec \_ Options proporciona un hglobal que contiene una estructura DSDISPLAYSPECOPTIONS.
ms.assetid: 98e033e4-14fe-44ed-83d5-a97e00ecce4c
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DS_DISPLAY_SPEC_OPTIONS
- CFSTR_DSDISPLAYSPECOPTIONS
api_location:
- DSClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d81f3a229971be5ecfb9ec2c86e166af27f94e01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079217"
---
# <a name="cfstr_ds_display_spec_options"></a><span data-ttu-id="5ad71-103">Opciones de presentación de CFSTR \_ DS \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="5ad71-103">CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS</span></span>

<dl> <dt>

<span data-ttu-id="5ad71-104"><span id="CFSTR_DS_DISPLAY_SPEC_OPTIONS"></span><span id="cfstr_ds_display_spec_options"></span>**Opciones de presentación de CFSTR \_ DS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5ad71-104"><span id="CFSTR_DS_DISPLAY_SPEC_OPTIONS"></span><span id="cfstr_ds_display_spec_options"></span>**CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ad71-105">"DsDisplaySpecOptions"</span><span class="sxs-lookup"><span data-stu-id="5ad71-105">"DsDisplaySpecOptions"</span></span>
</dt> <dt>



<span data-ttu-id="5ad71-106">Los Active Directory usuarios y equipos, los sitios Active Directory y los servicios, y los complementos dominios y confianzas de Active Directory admiten el formato del portapapeles **CFSTR \_ DS \_ Display \_ Spec \_ Options** .</span><span class="sxs-lookup"><span data-stu-id="5ad71-106">The Active Directory Users and Computers, the Active Directory Sites and Services, and the Active Directory Domains and Trusts snap-ins support the **CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS** clipboard format.</span></span> <span data-ttu-id="5ad71-107">El formato del portapapeles **CFSTR \_ DS \_ Display \_ Spec \_ Options** proporciona un **HGLOBAL** que contiene una estructura [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) .</span><span class="sxs-lookup"><span data-stu-id="5ad71-107">The **CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS** clipboard format provides an **HGLOBAL** that contains a [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) structure.</span></span> <span data-ttu-id="5ad71-108">**DSDISPLAYSPECOPTIONS** contiene datos de configuración para su uso por la extensión.</span><span class="sxs-lookup"><span data-stu-id="5ad71-108">The **DSDISPLAYSPECOPTIONS** contains configuration data for use by the extension.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ad71-109"><span id="CFSTR_DSDISPLAYSPECOPTIONS"></span><span id="cfstr_dsdisplayspecoptions"></span>**CFSTR \_ DSDISPLAYSPECOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="5ad71-109"><span id="CFSTR_DSDISPLAYSPECOPTIONS"></span><span id="cfstr_dsdisplayspecoptions"></span>**CFSTR\_DSDISPLAYSPECOPTIONS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5ad71-110">El formato del portapapeles de **CFSTR \_ DSDISPLAYSPECOPTIONS** es idéntico al formato del portapapeles de **CFSTR \_ DS \_ Display \_ Spec \_ Options** .</span><span class="sxs-lookup"><span data-stu-id="5ad71-110">The **CFSTR\_DSDISPLAYSPECOPTIONS** clipboard format is identical to the **CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS** clipboard format.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ad71-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ad71-111">Requirements</span></span>



| <span data-ttu-id="5ad71-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ad71-112">Requirement</span></span> | <span data-ttu-id="5ad71-113">Value</span><span class="sxs-lookup"><span data-stu-id="5ad71-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad71-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ad71-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5ad71-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ad71-115">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="5ad71-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ad71-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5ad71-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ad71-117">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="5ad71-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ad71-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ad71-119"><dt>DSClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ad71-119"><dt>DSClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ad71-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ad71-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ad71-121">**DSDISPLAYSPECOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="5ad71-121">**DSDISPLAYSPECOPTIONS**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions)
</dt> </dl>

 

 





