---
title: Constantes de WINBIO_SETTING_SOURCE (Winbio \_ Types. h)
description: Determine si el Plataforma de biometría de Windows está habilitado actualmente.
ms.assetid: d95aa6cc-ddff-40fb-ab82-eac78dc0cb6b
topic_type:
- apiref
api_name:
- WINBIO_SETTING_SOURCE_INVALID
- WINBIO_SETTING_SOURCE_DEFAULT
- WINBIO_SETTING_SOURCE_POLICY
- WINBIO_SETTING_SOURCE_LOCAL
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54723612c7e0948e09baddf22ad4f4703ca5c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997080"
---
# <a name="winbio_setting_source-constants"></a><span data-ttu-id="7cc90-103">Constantes de origen de \_ configuración de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="7cc90-103">WINBIO\_SETTING\_SOURCE Constants</span></span>

<span data-ttu-id="7cc90-104">La función [**WinBioGetEnabledSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) usa las constantes siguientes para determinar si el plataforma de biometría de Windows está habilitado actualmente.</span><span class="sxs-lookup"><span data-stu-id="7cc90-104">The following constants are used by the [**WinBioGetEnabledSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) function to determine whether the Windows Biometric Framework is currently enabled.</span></span> <span data-ttu-id="7cc90-105">Las constantes especifican dónde se originó la configuración.</span><span class="sxs-lookup"><span data-stu-id="7cc90-105">The constants specify where the setting originated.</span></span>



| <span data-ttu-id="7cc90-106">Constante</span><span class="sxs-lookup"><span data-stu-id="7cc90-106">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="7cc90-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="7cc90-107">Description</span></span>                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| <span id="WINBIO_SETTING_SOURCE_INVALID"></span><span id="winbio_setting_source_invalid"></span><dl> <span data-ttu-id="7cc90-108"><dt>**origen de configuración de WINBIO \_ \_ \_ no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="7cc90-108"><dt>**WINBIO\_SETTING\_SOURCE\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="7cc90-109">La configuración no es válida.</span><span class="sxs-lookup"><span data-stu-id="7cc90-109">The setting is not valid.</span></span><br/>                              |
| <span id="WINBIO_SETTING_SOURCE_DEFAULT"></span><span id="winbio_setting_source_default"></span><dl> <span data-ttu-id="7cc90-110"><dt>**valor \_ \_ predeterminado de origen de configuración WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7cc90-110"><dt>**WINBIO\_SETTING\_SOURCE\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="7cc90-111">La configuración se originó a partir de la Directiva integrada.</span><span class="sxs-lookup"><span data-stu-id="7cc90-111">The setting originated from built-in policy.</span></span><br/>           |
| <span id="WINBIO_SETTING_SOURCE_POLICY"></span><span id="winbio_setting_source_policy"></span><dl> <span data-ttu-id="7cc90-112"><dt>**configuración de la \_ \_ Directiva de origen de WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7cc90-112"><dt>**WINBIO\_SETTING\_SOURCE\_POLICY**</dt></span></span> </dl>    | <span data-ttu-id="7cc90-113">La configuración se originó en el registro del equipo local.</span><span class="sxs-lookup"><span data-stu-id="7cc90-113">The setting originated in the local computer registry.</span></span><br/> |
| <span id="WINBIO_SETTING_SOURCE_LOCAL"></span><span id="winbio_setting_source_local"></span><dl> <span data-ttu-id="7cc90-114"><dt>**WINBIO \_ configuración \_ local de origen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7cc90-114"><dt>**WINBIO\_SETTING\_SOURCE\_LOCAL**</dt></span></span> </dl>       | <span data-ttu-id="7cc90-115">La configuración fue creada por directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="7cc90-115">The setting was created by Group Policy</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="7cc90-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cc90-116">Requirements</span></span>



| <span data-ttu-id="7cc90-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cc90-117">Requirement</span></span> | <span data-ttu-id="7cc90-118">Value</span><span class="sxs-lookup"><span data-stu-id="7cc90-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cc90-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7cc90-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7cc90-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="7cc90-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="7cc90-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7cc90-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7cc90-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7cc90-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7cc90-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7cc90-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cc90-124"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7cc90-124"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cc90-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="7cc90-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cc90-126">Constantes de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="7cc90-126">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





