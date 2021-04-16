---
title: Estructura de WINBIO_REGISTERED_FORMAT (Winbio \_ Types. h)
description: Especifica un formato de datos registrado como par propietario/formato.
ms.assetid: a178840e-81cc-4dd3-9d80-a181fa7fa888
keywords:
- Plataforma de biometría de Windows API de WINBIO_REGISTERED_FORMAT Structure
- PWINBIO_REGISTERED_FORMAT de puntero de estructura Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_REGISTERED_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f45293fe95627c7dfad4c9c51eb7fa74ad1738c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534192"
---
# <a name="winbio_registered_format-structure"></a><span data-ttu-id="38e33-105">WINBIO \_ \_ estructura de formato registrada</span><span class="sxs-lookup"><span data-stu-id="38e33-105">WINBIO\_REGISTERED\_FORMAT structure</span></span>

<span data-ttu-id="38e33-106">La estructura de **\_ \_ formato registrada WINBIO** especifica un formato de datos registrado como par de propietario/formato.</span><span class="sxs-lookup"><span data-stu-id="38e33-106">The **WINBIO\_REGISTERED\_FORMAT** structure specifies a registered data format as an owner/format pair.</span></span>

## <a name="syntax"></a><span data-ttu-id="38e33-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38e33-107">Syntax</span></span>


```C++
typedef struct _WINBIO_REGISTERED_FORMAT {
  USHORT Owner;
  USHORT Type;
} WINBIO_REGISTERED_FORMAT, *PWINBIO_REGISTERED_FORMAT;
```



## <a name="members"></a><span data-ttu-id="38e33-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="38e33-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="38e33-109">**Propietario**</span><span class="sxs-lookup"><span data-stu-id="38e33-109">**Owner**</span></span>
</dt> <dd>

<span data-ttu-id="38e33-110">Un valor de propietario asignado de IBIA (Asociación del sector biométrico internacional).</span><span class="sxs-lookup"><span data-stu-id="38e33-110">An IBIA (International Biometric Industry Association) assigned owner value.</span></span>

</dd> <dt>

<span data-ttu-id="38e33-111">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="38e33-111">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="38e33-112">Formato asignado al propietario.</span><span class="sxs-lookup"><span data-stu-id="38e33-112">An owner assigned format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38e33-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38e33-113">Remarks</span></span>

<span data-ttu-id="38e33-114">Dado que Windows actualmente solo admite lectores de huellas digitales, se deben usar los valores siguientes en la estructura de **\_ \_ formato registrada WINBIO** .</span><span class="sxs-lookup"><span data-stu-id="38e33-114">Because Windows currently supports only fingerprint readers, the following values should be used in the **WINBIO\_REGISTERED\_FORMAT** structure.</span></span>



| <span data-ttu-id="38e33-115">Constante</span><span class="sxs-lookup"><span data-stu-id="38e33-115">Constant</span></span>                                    | <span data-ttu-id="38e33-116">Significado</span><span class="sxs-lookup"><span data-stu-id="38e33-116">Meaning</span></span>                                                                                                               |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38e33-117">WINBIO \_ \_ propietario de \_ formato ANSI 381 \_</span><span class="sxs-lookup"><span data-stu-id="38e33-117">WINBIO\_ANSI\_381\_FORMAT\_OWNER</span></span><br/> | <span data-ttu-id="38e33-118">Comité Internacional para el Comité técnico M1 (biométrico de estándares de tecnología de la información) (INCITS).</span><span class="sxs-lookup"><span data-stu-id="38e33-118">InterNational Committee for Information Technology Standards (INCITS) technical committee M1 (biometrics).</span></span><br/> |
| <span data-ttu-id="38e33-119">WINBIO \_ \_ tipo de \_ formato ANSI 381 \_</span><span class="sxs-lookup"><span data-stu-id="38e33-119">WINBIO\_ANSI\_381\_FORMAT\_TYPE</span></span><br/>  | <span data-ttu-id="38e33-120">Formato de intercambio de datos basado en imágenes de Finger ANSI INCITS 381.</span><span class="sxs-lookup"><span data-stu-id="38e33-120">ANSI INCITS 381 finger image based data interchange format.</span></span><br/>                                                |



 

## <a name="requirements"></a><span data-ttu-id="38e33-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38e33-121">Requirements</span></span>



| <span data-ttu-id="38e33-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="38e33-122">Requirement</span></span> | <span data-ttu-id="38e33-123">Value</span><span class="sxs-lookup"><span data-stu-id="38e33-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38e33-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38e33-124">Minimum supported client</span></span><br/> | <span data-ttu-id="38e33-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="38e33-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="38e33-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38e33-126">Minimum supported server</span></span><br/> | <span data-ttu-id="38e33-127">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="38e33-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="38e33-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38e33-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="38e33-129"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38e33-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38e33-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="38e33-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38e33-131">Estructuras de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="38e33-131">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="38e33-132">**WINBIO \_ \_ constantes de \_ formato ANSI 381**</span><span class="sxs-lookup"><span data-stu-id="38e33-132">**WINBIO\_ANSI\_381\_FORMAT Constants**</span></span>](winbio-ansi-381-format-constants.md)
</dt> <dt>

[<span data-ttu-id="38e33-133">**\_Encabezado WINBIO BDB \_ ANSI \_ 381 \_**</span><span class="sxs-lookup"><span data-stu-id="38e33-133">**WINBIO\_BDB\_ANSI\_381\_HEADER**</span></span>](winbio-bdb-ansi-381-header.md)
</dt> <dt>

[<span data-ttu-id="38e33-134">**WINBIO \_ \_ encabezado Bir**</span><span class="sxs-lookup"><span data-stu-id="38e33-134">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





