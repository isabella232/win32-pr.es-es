---
title: Constantes de WINBIO_FLAG (Winbio \_ Types. h)
description: Especifique la configuración de unidades biométricas y las características de acceso para la nueva sesión.
ms.assetid: 82b57023-6c27-433d-bf13-f136f501fc60
topic_type:
- apiref
api_name:
- WINBIO_FLAG_DEFAULT
- WINBIO_FLAG_BASIC
- WINBIO_FLAG_ADVANCED
- WINBIO_FLAG_RAW
- WINBIO_FLAG_MAINTENANCE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed632b5f15cc3d6a7ac6b0c6c70a2b3431b73db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422041"
---
# <a name="winbio_flag-constants"></a><span data-ttu-id="9b0d5-103">\_Constantes de marca WINBIO</span><span class="sxs-lookup"><span data-stu-id="9b0d5-103">WINBIO\_FLAG Constants</span></span>

<span data-ttu-id="9b0d5-104">Se pueden usar las siguientes constantes en la función [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) para especificar la configuración de unidad biométrica y las características de acceso para la nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="9b0d5-104">The following constants can be used in the [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) function to specify biometric unit configuration and access characteristics for the new session.</span></span>



| <span data-ttu-id="9b0d5-105">Constante</span><span class="sxs-lookup"><span data-stu-id="9b0d5-105">Constant</span></span>                                                                                                                                                                                     | <span data-ttu-id="9b0d5-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b0d5-106">Description</span></span>                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FLAG_DEFAULT"></span><span id="winbio_flag_default"></span><dl> <span data-ttu-id="9b0d5-107"><dt>**WINBIO \_ marca \_ predeterminada**</dt></span><span class="sxs-lookup"><span data-stu-id="9b0d5-107"><dt>**WINBIO\_FLAG\_DEFAULT**</dt></span></span> </dl>             | <span data-ttu-id="9b0d5-108">Marca de configuración del sensor.</span><span class="sxs-lookup"><span data-stu-id="9b0d5-108">Sensor configuration flag.</span></span> <span data-ttu-id="9b0d5-109">Las unidades biométricas funcionan de la manera especificada durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="9b0d5-109">The biometric units operate in the manner specified during installation.</span></span><br/>                                                                           |
| <span id="WINBIO_FLAG_BASIC"></span><span id="winbio_flag_basic"></span><dl> <span data-ttu-id="9b0d5-110"><dt>**marca de WINBIO \_ \_ básica**</dt></span><span class="sxs-lookup"><span data-stu-id="9b0d5-110"><dt>**WINBIO\_FLAG\_BASIC**</dt></span></span> </dl>                   | <span data-ttu-id="9b0d5-111">Marca de configuración del sensor.</span><span class="sxs-lookup"><span data-stu-id="9b0d5-111">Sensor configuration flag.</span></span> <span data-ttu-id="9b0d5-112">Las unidades biométricas funcionan solo como dispositivos de captura básicos.</span><span class="sxs-lookup"><span data-stu-id="9b0d5-112">The biometric units operate only as basic capture devices.</span></span><br/>                                                                                         |
| <span id="WINBIO_FLAG_ADVANCED"></span><span id="winbio_flag_advanced"></span><dl> <span data-ttu-id="9b0d5-113"><dt>**\_marca WINBIO \_ avanzada**</dt></span><span class="sxs-lookup"><span data-stu-id="9b0d5-113"><dt>**WINBIO\_FLAG\_ADVANCED**</dt></span></span> </dl>          | <span data-ttu-id="9b0d5-114">Marca de configuración del sensor.</span><span class="sxs-lookup"><span data-stu-id="9b0d5-114">Sensor configuration flag.</span></span> <span data-ttu-id="9b0d5-115">Las unidades biométricas usan funciones internas de procesamiento y almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="9b0d5-115">The biometric units use internal processing and storage capabilities.</span></span><br/>                                                                              |
| <span id="WINBIO_FLAG_RAW"></span><span id="winbio_flag_raw"></span><dl> <span data-ttu-id="9b0d5-116"><dt>**marca de WINBIO \_ \_ sin formato**</dt></span><span class="sxs-lookup"><span data-stu-id="9b0d5-116"><dt>**WINBIO\_FLAG\_RAW**</dt></span></span> </dl>                         | <span data-ttu-id="9b0d5-117">Marca de acceso deseada.</span><span class="sxs-lookup"><span data-stu-id="9b0d5-117">Desired access flag.</span></span> <span data-ttu-id="9b0d5-118">La aplicación cliente captura datos biométricos sin procesar mediante [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span><span class="sxs-lookup"><span data-stu-id="9b0d5-118">The client application captures raw biometric data using [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span></span><br/>                                             |
| <span id="WINBIO_FLAG_MAINTENANCE"></span><span id="winbio_flag_maintenance"></span><dl> <span data-ttu-id="9b0d5-119"><dt>**mantenimiento de la \_ marca WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9b0d5-119"><dt>**WINBIO\_FLAG\_MAINTENANCE**</dt></span></span> </dl> | <span data-ttu-id="9b0d5-120">Marca de acceso deseada.</span><span class="sxs-lookup"><span data-stu-id="9b0d5-120">Desired access flag.</span></span> <span data-ttu-id="9b0d5-121">El cliente realiza operaciones de control definidas por el proveedor en una unidad biométrica mediante una llamada a [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span><span class="sxs-lookup"><span data-stu-id="9b0d5-121">The client performs vendor-defined control operations on a biometric unit by calling [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9b0d5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b0d5-122">Requirements</span></span>



| <span data-ttu-id="9b0d5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b0d5-123">Requirement</span></span> | <span data-ttu-id="9b0d5-124">Value</span><span class="sxs-lookup"><span data-stu-id="9b0d5-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b0d5-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b0d5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9b0d5-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b0d5-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="9b0d5-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b0d5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9b0d5-128">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b0d5-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9b0d5-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b0d5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b0d5-130"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b0d5-130"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b0d5-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b0d5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b0d5-132">Constantes de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="9b0d5-132">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





