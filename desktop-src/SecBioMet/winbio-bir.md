---
title: Estructura de WINBIO_BIR (Winbio \_ Types. h)
description: Representa un registro de información biométrica (BIR).
ms.assetid: 39cfab34-0416-4897-bf95-a1b3c3a6a7a1
keywords:
- Plataforma de biometría de Windows API de WINBIO_BIR Structure
topic_type:
- apiref
api_name:
- WINBIO_BIR
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e422bbe59414d75541127b41e5e2cc1829adaaa7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686214"
---
# <a name="winbio_bir-structure"></a><span data-ttu-id="cf8ce-104">WINBIO \_ estructura Bir</span><span class="sxs-lookup"><span data-stu-id="cf8ce-104">WINBIO\_BIR structure</span></span>

<span data-ttu-id="cf8ce-105">La estructura **WINBIO \_ Bir** representa un registro de información biométrica (BIR).</span><span class="sxs-lookup"><span data-stu-id="cf8ce-105">The **WINBIO\_BIR** structure represents a biometric information record (BIR).</span></span> <span data-ttu-id="cf8ce-106">El registro de información contiene los bloques de encabezado, de datos y de firma.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-106">The information record contains header, data, and signature blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf8ce-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf8ce-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR {
  WINBIO_BIR_DATA HeaderBlock;
  WINBIO_BIR_DATA StandardDataBlock;
  WINBIO_BIR_DATA VendorDataBlock;
  WINBIO_BIR_DATA SignatureBlock;
} WINBIO_BIR;
```



## <a name="members"></a><span data-ttu-id="cf8ce-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="cf8ce-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="cf8ce-109">**HeaderBlock**</span><span class="sxs-lookup"><span data-stu-id="cf8ce-109">**HeaderBlock**</span></span>
</dt> <dd>

<span data-ttu-id="cf8ce-110">Una estructura de [**\_ \_ datos de WINBIO Bir**](winbio-bir-data.md) que contiene el tamaño, en bytes, y el desplazamiento del encabezado Bir.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-110">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of the BIR header.</span></span> <span data-ttu-id="cf8ce-111">El encabezado contiene información que describe el contenido del registro de información.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-111">The header contains information that describes the contents of the information record.</span></span>

</dd> <dt>

<span data-ttu-id="cf8ce-112">**StandardDataBlock**</span><span class="sxs-lookup"><span data-stu-id="cf8ce-112">**StandardDataBlock**</span></span>
</dt> <dd>

<span data-ttu-id="cf8ce-113">Una estructura de [**\_ \_ datos de WINBIO Bir**](winbio-bir-data.md) que contiene el tamaño, en bytes, y el desplazamiento de la información biométrica procesada o no procesada creada por el plataforma de biometría de Windows (WBF).</span><span class="sxs-lookup"><span data-stu-id="cf8ce-113">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of processed or unprocessed biometric information created by the Windows Biometric Framework (WBF).</span></span>

</dd> <dt>

<span data-ttu-id="cf8ce-114">**VendorDataBlock**</span><span class="sxs-lookup"><span data-stu-id="cf8ce-114">**VendorDataBlock**</span></span>
</dt> <dd>

<span data-ttu-id="cf8ce-115">Una estructura de [**\_ \_ datos de WINBIO Bir**](winbio-bir-data.md) que contiene el tamaño, en bytes, y el desplazamiento de la información biométrica procesada o no procesada proporcionada por los sensores y el software del proveedor.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-115">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of processed or unprocessed biometric information provided by vendor sensors and software.</span></span>

</dd> <dt>

<span data-ttu-id="cf8ce-116">**SignatureBlock**</span><span class="sxs-lookup"><span data-stu-id="cf8ce-116">**SignatureBlock**</span></span>
</dt> <dd>

<span data-ttu-id="cf8ce-117">Una estructura [**de \_ \_ datos WINBIO Bir**](winbio-bir-data.md) opcional que contiene el tamaño, en bytes, y el desplazamiento del código de autenticación de mensajes (Mac) de firma digital que se puede usar para comprobar la integridad de la Bir.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-117">An optional [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of the digital signature message authentication code (MAC) that can be used to verify the integrity of the BIR.</span></span> <span data-ttu-id="cf8ce-118">Si está presente, la firma o el MAC deben cubrir el encabezado y los bloques de datos.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-118">If present, the signature or MAC must cover the header and data blocks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf8ce-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf8ce-119">Remarks</span></span>

<span data-ttu-id="cf8ce-120">El uso de desplazamientos en lugar de punteros permite una sencilla serialización de BIR y para una traducción menos complicada entre los entornos 32 y 64-bit o entre el modo de usuario y kernel.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-120">The use of offsets rather than pointers allows for easy serialization of the BIR and for less complicated translation between 32 and 64-bit environments or between user and kernel mode.</span></span>

<span data-ttu-id="cf8ce-121">BIR es compatible con el marco de trabajo de intercambio biométrico común (CBEFF) definido por NIST 6529-A.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-121">The BIR is compatible with the Common Biometric Exchange Format Framework (CBEFF) defined by NIST 6529-A.</span></span>

<span data-ttu-id="cf8ce-122">Si esta estructura contiene un valor *StandardDataBlock* , el parámetro de *tipo* del encabezado especificado por el parámetro *HeaderBlock* debe establecerse en **el \_ \_ tipo de \_ formato \_ WINBIO ANSI 381**.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-122">If this structure contains a *StandardDataBlock* value, the *Type* parameter of the header specified by the *HeaderBlock* parameter must be set to **WINBIO\_ANSI\_381\_FORMAT\_TYPE**.</span></span> <span data-ttu-id="cf8ce-123">Este es el único formato de datos estándar que admite la versión actual de la Plataforma de biometría de Windows.</span><span class="sxs-lookup"><span data-stu-id="cf8ce-123">This is the only standard data format supported by the current version of the Windows Biometric Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf8ce-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf8ce-124">Requirements</span></span>



| <span data-ttu-id="cf8ce-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf8ce-125">Requirement</span></span> | <span data-ttu-id="cf8ce-126">Value</span><span class="sxs-lookup"><span data-stu-id="cf8ce-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf8ce-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf8ce-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cf8ce-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="cf8ce-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="cf8ce-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf8ce-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cf8ce-130">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cf8ce-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="cf8ce-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf8ce-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf8ce-132"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf8ce-132"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf8ce-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf8ce-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf8ce-134">Estructuras de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="cf8ce-134">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="cf8ce-135">**datos de WINBIO \_ Bir \_**</span><span class="sxs-lookup"><span data-stu-id="cf8ce-135">**WINBIO\_BIR\_DATA**</span></span>](winbio-bir-data.md)
</dt> <dt>

[<span data-ttu-id="cf8ce-136">**WINBIO \_ \_ encabezado Bir**</span><span class="sxs-lookup"><span data-stu-id="cf8ce-136">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





