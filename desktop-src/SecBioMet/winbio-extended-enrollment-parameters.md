---
title: Estructura de WINBIO_EXTENDED_ENROLLMENT_PARAMETERS (Winbio \_ Adapter. h)
description: Contiene información adicional que un adaptador de motor necesita para crear una plantilla de inscripción.
ms.assetid: E8007316-0A9D-4F35-A266-273B2406D545
keywords:
- Plataforma de biometría de Windows API de WINBIO_EXTENDED_ENROLLMENT_PARAMETERS Structure
- PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS de puntero de estructura Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f041d131bcee540a75a131b4179947fbe8e394
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489557"
---
# <a name="winbio_extended_enrollment_parameters-structure"></a><span data-ttu-id="d8265-105">WINBIO \_ \_ estructura de parámetros de inscripción extendida \_</span><span class="sxs-lookup"><span data-stu-id="d8265-105">WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS structure</span></span>

<span data-ttu-id="d8265-106">La estructura **WINBIO \_ Extended \_ ENROLLMENT \_ Parameters** contiene información adicional que un adaptador de motor necesita para crear una plantilla de inscripción.</span><span class="sxs-lookup"><span data-stu-id="d8265-106">The **WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS** structure contains additional information that an engine adapter needs to create an enrollment template.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8265-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8265-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_PARAMETERS {
  SIZE_T                   Size;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
} WINBIO_EXTENDED_ENROLLMENT_PARAMETERS, *PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="d8265-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d8265-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d8265-109">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="d8265-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="d8265-110">Tamaño (en bytes) de la estructura **WINBIO \_ Extended \_ ENROLLMENT \_ Parameters** .</span><span class="sxs-lookup"><span data-stu-id="d8265-110">The size (in bytes) of the **WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="d8265-111">**Subfactor**</span><span class="sxs-lookup"><span data-stu-id="d8265-111">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="d8265-112">Uno de los [**valores \_ constantes del \_ subtipo biométrico WINBIO**](winbio-biometric-subtype-constants.md) que proporciona información adicional sobre la inscripción.</span><span class="sxs-lookup"><span data-stu-id="d8265-112">One of the [**WINBIO\_BIOMETRIC\_SUBTYPE Constants**](winbio-biometric-subtype-constants.md) values that provides additional information about the enrollment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8265-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8265-113">Remarks</span></span>

<span data-ttu-id="d8265-114">El Plataforma de biometría de Windows pasa esta estructura al método [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) durante una operación de inscripción.</span><span class="sxs-lookup"><span data-stu-id="d8265-114">The Windows Biometric Framework passes this structure to the [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) method during an enrollment operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8265-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8265-115">Requirements</span></span>



| <span data-ttu-id="d8265-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8265-116">Requirement</span></span> | <span data-ttu-id="d8265-117">Value</span><span class="sxs-lookup"><span data-stu-id="d8265-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8265-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8265-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d8265-119">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="d8265-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="d8265-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8265-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d8265-121">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="d8265-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="d8265-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8265-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8265-123"><dt>Winbio \_ Adapter. h (incluir Winbio \_ Adapter. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8265-123"><dt>Winbio\_adapter.h (include Winbio\_adapter.h)</dt></span></span> </dl> |



 

 





