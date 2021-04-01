---
title: Constantes de WINBIO_DB (Winbio \_ Types. h)
description: Especifique la base de datos que se va a usar para un grupo de sistemas.
ms.assetid: 2cffa455-5834-4a35-b8d8-f9d1feddcaa1
topic_type:
- apiref
api_name:
- WINBIO_DB_DEFAULT
- WINBIO_DB_BOOTSTRAP
- WINBIO_DB_ONCHIP
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20503e1dc3cd7b5e47651889dd9c67777614593c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150515"
---
# <a name="winbio_db-constants"></a><span data-ttu-id="5a09c-103">Constantes de WINBIO \_ dB</span><span class="sxs-lookup"><span data-stu-id="5a09c-103">WINBIO\_DB Constants</span></span>

<span data-ttu-id="5a09c-104">Las siguientes constantes se pueden usar al llamar a [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) para especificar la base de datos que se va a usar para un grupo de sistema.</span><span class="sxs-lookup"><span data-stu-id="5a09c-104">The following constants can be used when calling [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) to specify the database to be used for a system pool.</span></span>



| <span data-ttu-id="5a09c-105">Constante</span><span class="sxs-lookup"><span data-stu-id="5a09c-105">Constant</span></span>                                                                                                                                                                         | <span data-ttu-id="5a09c-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a09c-106">Description</span></span>                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DB_DEFAULT"></span><span id="winbio_db_default"></span><dl> <span data-ttu-id="5a09c-107"><dt>**\_ \_ valor predeterminado de la base de WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="5a09c-107"><dt>**WINBIO\_DB\_DEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="5a09c-108">Cada unidad biométrica del grupo de sensores utiliza la base de datos predeterminada especificada en la configuración de unidad biométrica predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5a09c-108">Each biometric unit in the sensor pool uses the default database specified in the default biometric unit configuration.</span></span><br/>                                                                   |
| <span id="WINBIO_DB_BOOTSTRAP"></span><span id="winbio_db_bootstrap"></span><dl> <span data-ttu-id="5a09c-109"><dt>**BOOTSTRAP de WINBIO \_ dB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5a09c-109"><dt>**WINBIO\_DB\_BOOTSTRAP**</dt></span></span> </dl> | <span data-ttu-id="5a09c-110">Se puede usar para escenarios antes de iniciar Windows.</span><span class="sxs-lookup"><span data-stu-id="5a09c-110">Can be used for scenarios prior to starting Windows.</span></span> <span data-ttu-id="5a09c-111">Normalmente, la base de datos forma parte del chip del sensor o forma parte del BIOS y solo se puede usar para la inscripción y eliminación de plantillas.</span><span class="sxs-lookup"><span data-stu-id="5a09c-111">Typically, the database is part of the sensor chip or is part of the BIOS and can only be used for template enrollment and deletion.</span></span><br/> |
| <span id="WINBIO_DB_ONCHIP"></span><span id="winbio_db_onchip"></span><dl> <span data-ttu-id="5a09c-112"><dt>**WINBIO \_ dB en \_ chip**</dt></span><span class="sxs-lookup"><span data-stu-id="5a09c-112"><dt>**WINBIO\_DB\_ONCHIP**</dt></span></span> </dl>          | <span data-ttu-id="5a09c-113">La base de datos reside en el chip del sensor.</span><span class="sxs-lookup"><span data-stu-id="5a09c-113">The database resides on the sensor chip.</span></span><br/>                                                                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="5a09c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a09c-114">Requirements</span></span>



| <span data-ttu-id="5a09c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a09c-115">Requirement</span></span> | <span data-ttu-id="5a09c-116">Value</span><span class="sxs-lookup"><span data-stu-id="5a09c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a09c-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a09c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5a09c-118">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a09c-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="5a09c-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a09c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5a09c-120">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a09c-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5a09c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a09c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a09c-122"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a09c-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a09c-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a09c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a09c-124">Constantes de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="5a09c-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





