---
title: Estructura de WINBIO_BIR_DATA (Winbio \_ Types. h)
description: Especifica el tamaño, en bytes, y el desplazamiento de un bloque de información biométrica.
ms.assetid: 2f73eb1f-f1a1-4831-a8f7-eec28aa51645
keywords:
- Plataforma de biometría de Windows API de WINBIO_BIR_DATA Structure
topic_type:
- apiref
api_name:
- WINBIO_BIR_DATA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41ebf7b157c5bd806442cdc120350a89ce646f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422282"
---
# <a name="winbio_bir_data-structure"></a><span data-ttu-id="d0392-104">Estructura de datos de WINBIO \_ Bir \_</span><span class="sxs-lookup"><span data-stu-id="d0392-104">WINBIO\_BIR\_DATA structure</span></span>

<span data-ttu-id="d0392-105">La estructura de **\_ \_ datos de WINBIO Bir** especifica el tamaño, en bytes, y el desplazamiento de un bloque de información biométrica.</span><span class="sxs-lookup"><span data-stu-id="d0392-105">The **WINBIO\_BIR\_DATA** structure specifies the size, in bytes, and the offset of a block of biometric information.</span></span> <span data-ttu-id="d0392-106">La estructura [**WINBIO \_ Bir**](winbio-bir.md) usa esta estructura para especificar dónde se encuentran las distintas partes de un registro de información biométrica.</span><span class="sxs-lookup"><span data-stu-id="d0392-106">This structure is used by the [**WINBIO\_BIR**](winbio-bir.md) structure to specify where the various parts of a biometric information record are located.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0392-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0392-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR_DATA {
  ULONG Size;
  ULONG Offset;
} WINBIO_BIR_DATA;
```



## <a name="members"></a><span data-ttu-id="d0392-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d0392-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d0392-109">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="d0392-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="d0392-110">Tamaño, en bytes, de la información biométrica.</span><span class="sxs-lookup"><span data-stu-id="d0392-110">Size, in bytes, of the biometric information.</span></span>

</dd> <dt>

<span data-ttu-id="d0392-111">**Offset**</span><span class="sxs-lookup"><span data-stu-id="d0392-111">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="d0392-112">Desplazamiento, en bytes desde el principio de la estructura de [**\_ Bir de WINBIO**](winbio-bir.md) , de la información de biométrica.</span><span class="sxs-lookup"><span data-stu-id="d0392-112">Offset, in bytes from the beginning of the [**WINBIO\_BIR**](winbio-bir.md) structure, of the biometric information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0392-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0392-113">Remarks</span></span>

<span data-ttu-id="d0392-114">El uso de desplazamientos en lugar de punteros permite una sencilla serialización de BIR y para una traducción menos complicada entre los entornos 32 y 64-bit o entre el modo de usuario y kernel.</span><span class="sxs-lookup"><span data-stu-id="d0392-114">The use of offsets rather than pointers allows for easy serialization of the BIR and for less complicated translation between 32 and 64-bit environments or between user and kernel mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0392-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0392-115">Requirements</span></span>



| <span data-ttu-id="d0392-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0392-116">Requirement</span></span> | <span data-ttu-id="d0392-117">Value</span><span class="sxs-lookup"><span data-stu-id="d0392-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0392-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0392-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d0392-119">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0392-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="d0392-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0392-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d0392-121">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0392-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d0392-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0392-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0392-123"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0392-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0392-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0392-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0392-125">Estructuras de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="d0392-125">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="d0392-126">**WINBIO \_ Bir**</span><span class="sxs-lookup"><span data-stu-id="d0392-126">**WINBIO\_BIR**</span></span>](winbio-bir.md)
</dt> <dt>

[<span data-ttu-id="d0392-127">**WINBIO \_ \_ encabezado Bir**</span><span class="sxs-lookup"><span data-stu-id="d0392-127">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





