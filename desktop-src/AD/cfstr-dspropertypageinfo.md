---
title: CFSTR_DSPROPERTYPAGEINFO (DSClient. h)
description: El \_ formato del portapapeles de CFSTR DSPROPERTYPAGEINFO proporciona un hglobal que contiene una estructura DSPROPERTYPAGEINFO.
ms.assetid: 84ed1322-fee3-44ee-873e-57586261ff62
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSPROPERTYPAGEINFO
api_location:
- DSClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 259c9addbb3ee41c7b12cd7ea77eb8393b69daaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079214"
---
# <a name="cfstr_dspropertypageinfo"></a><span data-ttu-id="27554-103">CFSTR \_ DSPROPERTYPAGEINFO</span><span class="sxs-lookup"><span data-stu-id="27554-103">CFSTR\_DSPROPERTYPAGEINFO</span></span>

<dl> <dt>

<span data-ttu-id="27554-104"><span id="CFSTR_DSPROPERTYPAGEINFO"></span><span id="cfstr_dspropertypageinfo"></span>**CFSTR \_ DSPROPERTYPAGEINFO**</span><span class="sxs-lookup"><span data-stu-id="27554-104"><span id="CFSTR_DSPROPERTYPAGEINFO"></span><span id="cfstr_dspropertypageinfo"></span>**CFSTR\_DSPROPERTYPAGEINFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27554-105">"DsPropPageInfo"</span><span class="sxs-lookup"><span data-stu-id="27554-105">"DsPropPageInfo"</span></span>
</dt> <dt>



<span data-ttu-id="27554-106">El formato del portapapeles de **CFSTR \_ DSPROPERTYPAGEINFO** proporciona un **HGLOBAL** que contiene una estructura [**DSPROPERTYPAGEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) .</span><span class="sxs-lookup"><span data-stu-id="27554-106">The **CFSTR\_DSPROPERTYPAGEINFO** clipboard format provides an **HGLOBAL** that contains a [**DSPROPERTYPAGEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) structure.</span></span> <span data-ttu-id="27554-107">La estructura **DSPROPERTYPAGEINFO** contiene la cadena opcional que la extensión agregó a los valores de los parámetros **adminPropertySheet** y/o **shellPropertySheet** cuando se registró la extensión.</span><span class="sxs-lookup"><span data-stu-id="27554-107">The **DSPROPERTYPAGEINFO** structure contains the optional string that the extension added to the **adminPropertySheet** and/or **shellPropertySheet** parameter values when the extension was registered.</span></span> <span data-ttu-id="27554-108">Para obtener más información sobre cómo se establece esta cadena, vea [registrar la página de propiedades de un objeto com en un especificador de presentación](registering-the-property-page-com-object-in-a-display-specifier.md).</span><span class="sxs-lookup"><span data-stu-id="27554-108">For more information about how this string is set, see [Registering the Property Page COM Object in a Display Specifier](registering-the-property-page-com-object-in-a-display-specifier.md).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27554-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27554-109">Requirements</span></span>



| <span data-ttu-id="27554-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="27554-110">Requirement</span></span> | <span data-ttu-id="27554-111">Value</span><span class="sxs-lookup"><span data-stu-id="27554-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27554-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27554-112">Minimum supported client</span></span><br/> | <span data-ttu-id="27554-113">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27554-113">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="27554-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27554-114">Minimum supported server</span></span><br/> | <span data-ttu-id="27554-115">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27554-115">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="27554-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27554-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="27554-117"><dt>DSClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="27554-117"><dt>DSClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27554-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="27554-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27554-119">**DSPROPERTYPAGEINFO**</span><span class="sxs-lookup"><span data-stu-id="27554-119">**DSPROPERTYPAGEINFO**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo)
</dt> <dt>

[<span data-ttu-id="27554-120">Registrar el objeto COM de la página de propiedades en un especificador de presentación</span><span class="sxs-lookup"><span data-stu-id="27554-120">Registering the Property Page COM Object in a Display Specifier</span></span>](registering-the-property-page-com-object-in-a-display-specifier.md)
</dt> </dl>

 

 





