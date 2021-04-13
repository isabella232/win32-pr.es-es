---
title: Estructura de WINBIO_BDB_ANSI_381_RECORD (Winbio \_ Types. h)
description: Contiene información sobre una sola huella digital o un ejemplo de Palm de un usuario final.
ms.assetid: e0b32d05-3e96-4b42-9e18-57d10513f224
keywords:
- Plataforma de biometría de Windows API de WINBIO_BDB_ANSI_381_RECORD Structure
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_RECORD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30af31d88349dbe02066f231cdff21293aebe90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421971"
---
# <a name="winbio_bdb_ansi_381_record-structure"></a><span data-ttu-id="33670-104">\_Estructura de registro WINBIO BDB \_ ANSI \_ 381 \_</span><span class="sxs-lookup"><span data-stu-id="33670-104">WINBIO\_BDB\_ANSI\_381\_RECORD structure</span></span>

<span data-ttu-id="33670-105">La estructura de **\_ registro WINBIO BDB \_ ANSI \_ 381 \_** contiene información sobre una sola huella digital o un ejemplo de Palm de un usuario final.</span><span class="sxs-lookup"><span data-stu-id="33670-105">The **WINBIO\_BDB\_ANSI\_381\_RECORD** structure contains information about a single fingerprint or palm sample from an end user.</span></span> <span data-ttu-id="33670-106">Se incluye una colección de estas estructuras en cada estructura de [**\_ encabezado WINBIO BDB \_ ANSI \_ 381 \_**](winbio-bdb-ansi-381-header.md) .</span><span class="sxs-lookup"><span data-stu-id="33670-106">A collection of these structures is included in each [**WINBIO\_BDB\_ANSI\_381\_HEADER**](winbio-bdb-ansi-381-header.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="33670-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33670-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BDB_ANSI_381_RECORD {
  ULONG                    BlockLength;
  USHORT                   HorizontalLineLength;
  USHORT                   VerticalLineLength;
  WINBIO_BIOMETRIC_SUBTYPE Position;
  UCHAR                    CountOfViews;
  UCHAR                    ViewNumber;
  UCHAR                    ImageQuality;
  UCHAR                    ImpressionType;
  UCHAR                    Reserved;
} WINBIO_BDB_ANSI_381_RECORD;
```



## <a name="members"></a><span data-ttu-id="33670-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="33670-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="33670-109">**BlockLength**</span><span class="sxs-lookup"><span data-stu-id="33670-109">**BlockLength**</span></span>
</dt> <dd>

<span data-ttu-id="33670-110">Contiene el número de bytes de esta estructura más el número de bytes de datos de imagen de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="33670-110">Contains the number of bytes in this structure plus the number of bytes of sample image data.</span></span>

</dd> <dt>

<span data-ttu-id="33670-111">**HorizontalLineLength**</span><span class="sxs-lookup"><span data-stu-id="33670-111">**HorizontalLineLength**</span></span>
</dt> <dd>

<span data-ttu-id="33670-112">Especifica el número de píxeles en una línea horizontal del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="33670-112">Specifies the number of pixels in a horizontal line of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="33670-113">**VerticalLineLength**</span><span class="sxs-lookup"><span data-stu-id="33670-113">**VerticalLineLength**</span></span>
</dt> <dd>

<span data-ttu-id="33670-114">Especifica el número de píxeles en una línea vertical del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="33670-114">Specifies the number of pixels in a vertical line of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="33670-115">**Position**</span><span class="sxs-lookup"><span data-stu-id="33670-115">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="33670-116">Un valor de **\_ \_ subtipo biométrico WINBIO** que especifica el dedo o la palma utilizada para generar el ejemplo biométrico.</span><span class="sxs-lookup"><span data-stu-id="33670-116">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that specifies the finger or palm used to generate the biometric sample.</span></span> <span data-ttu-id="33670-117">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="33670-117">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="33670-118">**CountOfViews**</span><span class="sxs-lookup"><span data-stu-id="33670-118">**CountOfViews**</span></span>
</dt> <dd>

<span data-ttu-id="33670-119">Debe establecerse en uno (1);</span><span class="sxs-lookup"><span data-stu-id="33670-119">This must be set to one (1);</span></span>

</dd> <dt>

<span data-ttu-id="33670-120">**ViewNumber**</span><span class="sxs-lookup"><span data-stu-id="33670-120">**ViewNumber**</span></span>
</dt> <dd>

<span data-ttu-id="33670-121">Debe establecerse en uno (1);</span><span class="sxs-lookup"><span data-stu-id="33670-121">This must be set to one (1);</span></span>

</dd> <dt>

<span data-ttu-id="33670-122">**ImageQuality**</span><span class="sxs-lookup"><span data-stu-id="33670-122">**ImageQuality**</span></span>
</dt> <dd>

<span data-ttu-id="33670-123">Reservado.</span><span class="sxs-lookup"><span data-stu-id="33670-123">Reserved.</span></span> <span data-ttu-id="33670-124">Debe ser 254 (0xFE).</span><span class="sxs-lookup"><span data-stu-id="33670-124">This must be 254 (0xFE).</span></span>

</dd> <dt>

<span data-ttu-id="33670-125">**ImpressionType**</span><span class="sxs-lookup"><span data-stu-id="33670-125">**ImpressionType**</span></span>
</dt> <dd>

<span data-ttu-id="33670-126">Reservado.</span><span class="sxs-lookup"><span data-stu-id="33670-126">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="33670-127">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="33670-127">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="33670-128">Reservado.</span><span class="sxs-lookup"><span data-stu-id="33670-128">Reserved.</span></span> <span data-ttu-id="33670-129">Debe establecerse en cero (0).</span><span class="sxs-lookup"><span data-stu-id="33670-129">Must be set to zero (0).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33670-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33670-130">Remarks</span></span>

<span data-ttu-id="33670-131">El miembro *posición* especifica el área de la mano o la palma utilizada para crear el ejemplo biométrico.</span><span class="sxs-lookup"><span data-stu-id="33670-131">The *Position* member specifies the area of the hand or palm used to make the biometric sample.</span></span> <span data-ttu-id="33670-132">El Plataforma de biometría de Windows (WBF) actualmente solo admite la captura de huellas digitales y usa las siguientes constantes para representar la información de posición.</span><span class="sxs-lookup"><span data-stu-id="33670-132">The Windows Biometric Framework (WBF) currently supports only fingerprint capture and uses the following constants to represent position information.</span></span>

-   <span data-ttu-id="33670-133">WINBIO \_ ANSI \_ 381 \_ pos \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="33670-133">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="33670-134">\_Thumb WINBIO ANSI \_ 381 \_ pos \_ RH \_</span><span class="sxs-lookup"><span data-stu-id="33670-134">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="33670-135">\_Dedo de \_ \_ \_ \_ índice RH \_ de WINBIO ANSI 381 pos</span><span class="sxs-lookup"><span data-stu-id="33670-135">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="33670-136">\_Dedo central de WINBIO ANSI \_ 381 \_ pos \_ dcha \_ \_</span><span class="sxs-lookup"><span data-stu-id="33670-136">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="33670-137">\_Dedo de \_ \_ \_ \_ anillo RH \_ de WINBIO ANSI 381 pos</span><span class="sxs-lookup"><span data-stu-id="33670-137">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="33670-138">\_ \_ \_ \_ \_ Pequeño \_ dedo de WINBIO ANSI 381 pos</span><span class="sxs-lookup"><span data-stu-id="33670-138">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="33670-139">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Thumb</span><span class="sxs-lookup"><span data-stu-id="33670-139">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="33670-140">WINBIO \_ de \_ Índice de LH de pdv ANSI 381 \_ pos \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="33670-140">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="33670-141">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ central \_</span><span class="sxs-lookup"><span data-stu-id="33670-141">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="33670-142">WINBIO \_ el \_ \_ dedo de \_ anillo de LH ANSI 381 pos \_ \_</span><span class="sxs-lookup"><span data-stu-id="33670-142">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="33670-143">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Little \_ Finger</span><span class="sxs-lookup"><span data-stu-id="33670-143">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="33670-144">WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ cuatro \_ dedos</span><span class="sxs-lookup"><span data-stu-id="33670-144">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="33670-145">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ cuatro \_ dedos</span><span class="sxs-lookup"><span data-stu-id="33670-145">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="33670-146">WINBIO \_ ANSI \_ 381 \_ pos \_ dos \_ Thumbs</span><span class="sxs-lookup"><span data-stu-id="33670-146">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="33670-147">No intente validar el valor proporcionado para el valor de *posición* .</span><span class="sxs-lookup"><span data-stu-id="33670-147">Do not attempt to validate the value supplied for the *Position* value.</span></span> <span data-ttu-id="33670-148">El servicio biométrico de Windows validará el valor proporcionado antes de pasarlo a su implementación.</span><span class="sxs-lookup"><span data-stu-id="33670-148">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="33670-149">Si el valor es **WINBIO \_ SubType \_ no \_ Information** o **WINBIO \_ SubType \_ any**, valide cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="33670-149">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="33670-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33670-150">Requirements</span></span>



| <span data-ttu-id="33670-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="33670-151">Requirement</span></span> | <span data-ttu-id="33670-152">Value</span><span class="sxs-lookup"><span data-stu-id="33670-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33670-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33670-153">Minimum supported client</span></span><br/> | <span data-ttu-id="33670-154">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="33670-154">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="33670-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33670-155">Minimum supported server</span></span><br/> | <span data-ttu-id="33670-156">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="33670-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="33670-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="33670-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="33670-158"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33670-158"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33670-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="33670-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33670-160">Estructuras de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="33670-160">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





