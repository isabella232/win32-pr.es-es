---
title: Estructura de WINBIO_EXTENDED_STORAGE_INFO (Winbio \_ Types. h)
description: Contiene información acerca de las capacidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica.
ms.assetid: 7A648610-E947-4967-A9AF-C8A9C0B81D92
keywords:
- Plataforma de biometría de Windows API de WINBIO_EXTENDED_STORAGE_INFO Structure
- PWINBIO_EXTENDED_STORAGE_INFO de puntero de estructura Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_STORAGE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ac2559717a2040cfb617e85e0a51495be1b5987
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996037"
---
# <a name="winbio_extended_storage_info-structure"></a><span data-ttu-id="8b645-105">WINBIO \_ \_ estructura de información de almacenamiento extendido \_</span><span class="sxs-lookup"><span data-stu-id="8b645-105">WINBIO\_EXTENDED\_STORAGE\_INFO structure</span></span>

<span data-ttu-id="8b645-106">Contiene información acerca de las capacidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="8b645-106">Contains information about the capabilities and enrollment requirements of the storage adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b645-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b645-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_STORAGE_INFO {
  WINBIO_CAPABILITIES   GenericStorageCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_STORAGE_INFO, *PWINBIO_EXTENDED_STORAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="8b645-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8b645-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8b645-109">**GenericStorageCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8b645-109">**GenericStorageCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="8b645-110">Las capacidades genéricas del componente de almacenamiento que está conectado a una unidad biométrica específica.</span><span class="sxs-lookup"><span data-stu-id="8b645-110">The generic capabilities of the storage component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="8b645-111">**Factor**</span><span class="sxs-lookup"><span data-stu-id="8b645-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="8b645-112">El tipo de unidad biométrica para la que esta estructura contiene información acerca de las capacidades y los requisitos de inscripción del adaptador de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="8b645-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the storage adapter.</span></span> <span data-ttu-id="8b645-113">Por ejemplo, si el valor del miembro **factor** es **WINBIO \_ Type \_ FINGERPRINT**, la estructura de **\_ \_ \_ información de almacenamiento extendido WINBIO** se aplica a un lector de huellas digitales y contiene la información pertinente en la estructura **específico. FINGERPRINT** .</span><span class="sxs-lookup"><span data-stu-id="8b645-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_STORAGE\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="8b645-114">**Cuestión**</span><span class="sxs-lookup"><span data-stu-id="8b645-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="8b645-115">Información acerca de las capacidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica relacionada con un factor biométrico específico.</span><span class="sxs-lookup"><span data-stu-id="8b645-115">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="8b645-116">**Null**</span><span class="sxs-lookup"><span data-stu-id="8b645-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="8b645-117">Reservado.</span><span class="sxs-lookup"><span data-stu-id="8b645-117">Reserved.</span></span> <span data-ttu-id="8b645-118">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8b645-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8b645-119">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="8b645-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="8b645-120">Información acerca de las capacidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica relacionada con las características faciales.</span><span class="sxs-lookup"><span data-stu-id="8b645-120">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="8b645-121">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="8b645-121">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="8b645-122">Las capacidades de reconocimiento facial del componente de almacenamiento que está conectado a una unidad biométrica específica.</span><span class="sxs-lookup"><span data-stu-id="8b645-122">The facial recognition capabilities of the storage component that is connected to a specific biometric unit.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8b645-123">**Huella digital**</span><span class="sxs-lookup"><span data-stu-id="8b645-123">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="8b645-124">Información acerca de las capacidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica relacionada con patrones de huellas digitales.</span><span class="sxs-lookup"><span data-stu-id="8b645-124">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="8b645-125">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="8b645-125">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="8b645-126">Las funcionalidades de reconocimiento de huellas digitales del componente de almacenamiento que está conectado a una unidad biométrica específica</span><span class="sxs-lookup"><span data-stu-id="8b645-126">The fingerprint recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8b645-127">**Iris**</span><span class="sxs-lookup"><span data-stu-id="8b645-127">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="8b645-128">Información acerca de las capacidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica relacionada con los patrones de iris.</span><span class="sxs-lookup"><span data-stu-id="8b645-128">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="8b645-129">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="8b645-129">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="8b645-130">Las capacidades de reconocimiento de iris del componente de almacenamiento que está conectado a una unidad biométrica específica</span><span class="sxs-lookup"><span data-stu-id="8b645-130">The iris recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8b645-131">**Voz**</span><span class="sxs-lookup"><span data-stu-id="8b645-131">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="8b645-132">Información acerca de las capacidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica relacionada con los patrones de voz.</span><span class="sxs-lookup"><span data-stu-id="8b645-132">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="8b645-133">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="8b645-133">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="8b645-134">Las capacidades de reconocimiento de voz del componente de almacenamiento que está conectado a una unidad biométrica específica</span><span class="sxs-lookup"><span data-stu-id="8b645-134">The voice recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b645-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b645-135">Requirements</span></span>



| <span data-ttu-id="8b645-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b645-136">Requirement</span></span> | <span data-ttu-id="8b645-137">Value</span><span class="sxs-lookup"><span data-stu-id="8b645-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b645-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b645-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8b645-139">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="8b645-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="8b645-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b645-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8b645-141">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="8b645-141">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="8b645-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b645-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b645-143"><dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="8b645-143"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b645-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b645-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b645-145">**WINBIO \_ constantes de \_ tipo biométrico**</span><span class="sxs-lookup"><span data-stu-id="8b645-145">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> <dt>

[<span data-ttu-id="8b645-146">**Constantes de capacidad de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="8b645-146">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> </dl>

 

 





