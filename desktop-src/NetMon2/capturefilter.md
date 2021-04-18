---
description: La estructura CAPTUREFILTER contiene datos de filtro de captura.
ms.assetid: 773187c6-31c7-4439-850d-1dd43d42f701
title: Estructura CAPTUREFILTER (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILTER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 129575ba401aed0e78f52695a49139f4143c9c87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667742"
---
# <a name="capturefilter-structure"></a><span data-ttu-id="bfd69-103">Estructura CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="bfd69-103">CAPTUREFILTER structure</span></span>

<span data-ttu-id="bfd69-104">La estructura **CAPTUREFILTER** contiene datos de filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="bfd69-104">The **CAPTUREFILTER** structure contains capture filter data.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfd69-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfd69-105">Syntax</span></span>


```C++
typedef struct _CAPTUREFILTER {
  DWORD          FilterFlags;
  LPBYTE         lpSapTable;
  LPWORD         lpEtypeTable;
  WORD           nSaps;
  WORD           nEtypes;
  LPADDRESSTABLE AddressTable;
  EXPRESSION     FilterExpression;
  TRIGGER        Trigger;
  DWORD          nFrameBytesToCopy;
  RESERVED       Reserved;
} CAPTUREFILTER, *LPCAPTUREFILTER;
```



## <a name="members"></a><span data-ttu-id="bfd69-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="bfd69-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bfd69-107">**FilterFlags**</span><span class="sxs-lookup"><span data-stu-id="bfd69-107">**FilterFlags**</span></span>
</dt> <dd>

<span data-ttu-id="bfd69-108">Marcas que describen el contenido del filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="bfd69-108">Flags that describe the contents of the capture filter.</span></span>



| <span data-ttu-id="bfd69-109">Value</span><span class="sxs-lookup"><span data-stu-id="bfd69-109">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="bfd69-110">Significado</span><span class="sxs-lookup"><span data-stu-id="bfd69-110">Meaning</span></span>                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_SAPS"></span><span id="capturefilter_flags_include_all_saps"></span><dl> <span data-ttu-id="bfd69-111"><dt>**CAPTUREFILTER \_ \_Las marcas incluyen \_ todos los \_**</dt> <dt>0x0001</dt> de SAP</span><span class="sxs-lookup"><span data-stu-id="bfd69-111"><dt>**CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS**</dt> <dt>0x0001</dt></span></span> </dl>       | <span data-ttu-id="bfd69-112">Incluye todos los SAP como fotogramas aceptables.</span><span class="sxs-lookup"><span data-stu-id="bfd69-112">Includes all SAPs as acceptable frames.</span></span><br/>  |
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_ETYPES"></span><span id="capturefilter_flags_include_all_etypes"></span><dl> <span data-ttu-id="bfd69-113"><dt>**CAPTUREFILTER \_ \_Las marcas incluyen \_ All \_ ETYPE**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="bfd69-113"><dt>**CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="bfd69-114">Incluya todos los ETYPE como fotogramas aceptables.</span><span class="sxs-lookup"><span data-stu-id="bfd69-114">Include all Etypes as acceptable frames.</span></span><br/> |
| <span id="CAPTUREFILTER_FLAGS_LOCAL_ONLY"></span><span id="capturefilter_flags_local_only"></span><dl> <span data-ttu-id="bfd69-115"><dt>**CAPTUREFILTER \_ MARCAS \_ \_ solo locales**</dt> de <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="bfd69-115"><dt>**CAPTUREFILTER\_FLAGS\_LOCAL\_ONLY**</dt> <dt>0x0008</dt></span></span> </dl>                          | <span data-ttu-id="bfd69-116">Sin modo P</span><span class="sxs-lookup"><span data-stu-id="bfd69-116">No P-mode</span></span><br/>                                |
| <span id="CAPTUREFILTER_FLAGS_KEEP_RAW"></span><span id="capturefilter_flags_keep_raw"></span><dl> <span data-ttu-id="bfd69-117"><dt>**CAPTUREFILTER \_ Las marcas \_ mantienen 0x0020 \_ sin procesar**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bfd69-117"><dt>**CAPTUREFILTER\_FLAGS\_KEEP\_RAW**</dt> <dt>0x0020</dt></span></span> </dl>                                | <span data-ttu-id="bfd69-118">Mantenga fotogramas de SMT y tokens de MAC en anillo.</span><span class="sxs-lookup"><span data-stu-id="bfd69-118">Keep SMT and token ring MAC frames.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="bfd69-119">**lpSapTable**</span><span class="sxs-lookup"><span data-stu-id="bfd69-119">**lpSapTable**</span></span>
</dt> <dd>

<span data-ttu-id="bfd69-120">Puntero a una matriz de valores de SAP.</span><span class="sxs-lookup"><span data-stu-id="bfd69-120">Pointer to an array of SAP values.</span></span> <span data-ttu-id="bfd69-121">Este miembro indica los valores de SAP que son válidos para pasar al controlador.</span><span class="sxs-lookup"><span data-stu-id="bfd69-121">This member indicates the SAP values that are valid to pass to the driver.</span></span> <span data-ttu-id="bfd69-122">Si \_ las marcas \_ de CAPTUREFILTER incluyen \_ \_ la configuración de todos los SAP, se convierte en una lista de excepciones (incluye todos los SAP excepto estos).</span><span class="sxs-lookup"><span data-stu-id="bfd69-122">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS is set, this becomes an exception list (include all SAPS except these).</span></span>

</dd> <dt>

<span data-ttu-id="bfd69-123">**lpEtypeTable**</span><span class="sxs-lookup"><span data-stu-id="bfd69-123">**lpEtypeTable**</span></span>
</dt> <dd>

<span data-ttu-id="bfd69-124">Puntero a una matriz de valores ETYPE.</span><span class="sxs-lookup"><span data-stu-id="bfd69-124">Pointer to an array of Etype values.</span></span> <span data-ttu-id="bfd69-125">Indica los valores ETYPE que son válidos para pasar al controlador.</span><span class="sxs-lookup"><span data-stu-id="bfd69-125">This indicates those Etype values that are valid to pass to the driver.</span></span> <span data-ttu-id="bfd69-126">Si \_ las marcas \_ de CAPTUREFILTER incluyen \_ \_ la configuración de ETYPE, se convierte en una lista de excepciones (incluye todos los ETYPE excepto estos).</span><span class="sxs-lookup"><span data-stu-id="bfd69-126">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES is set, this becomes an exception list (include all Etypes except these).</span></span>

</dd> <dt>

<span data-ttu-id="bfd69-127">**nSaps**</span><span class="sxs-lookup"><span data-stu-id="bfd69-127">**nSaps**</span></span>
</dt> <dd>

<span data-ttu-id="bfd69-128">Número de SAP en la tabla de SAP.</span><span class="sxs-lookup"><span data-stu-id="bfd69-128">Number of SAPs in the SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="bfd69-129">**nEtypes**</span><span class="sxs-lookup"><span data-stu-id="bfd69-129">**nEtypes**</span></span>
</dt> <dd>

<span data-ttu-id="bfd69-130">Número de ETYPE en la tabla ETYPE.</span><span class="sxs-lookup"><span data-stu-id="bfd69-130">Number of Etypes in the Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="bfd69-131">**AddressTable**</span><span class="sxs-lookup"><span data-stu-id="bfd69-131">**AddressTable**</span></span>
</dt> <dd>

<span data-ttu-id="bfd69-132">Nombre de la tabla de direcciones.</span><span class="sxs-lookup"><span data-stu-id="bfd69-132">Name of the address table.</span></span>

</dd> <dt>

<span data-ttu-id="bfd69-133">**FilterExpression**</span><span class="sxs-lookup"><span data-stu-id="bfd69-133">**FilterExpression**</span></span>
</dt> <dd>

<span data-ttu-id="bfd69-134">Una estructura de expresión.</span><span class="sxs-lookup"><span data-stu-id="bfd69-134">An EXPRESSION structure.</span></span> <span data-ttu-id="bfd69-135">Contiene la parte de la coincidencia de patrones del filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="bfd69-135">This contains the pattern match portion of the capture filter.</span></span>

</dd> <dt>

<span data-ttu-id="bfd69-136">**Desencadenador**</span><span class="sxs-lookup"><span data-stu-id="bfd69-136">**Trigger**</span></span>
</dt> <dd>

<span data-ttu-id="bfd69-137">Reservado.</span><span class="sxs-lookup"><span data-stu-id="bfd69-137">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bfd69-138">**nFrameBytesToCopy**</span><span class="sxs-lookup"><span data-stu-id="bfd69-138">**nFrameBytesToCopy**</span></span>
</dt> <dd>

<span data-ttu-id="bfd69-139">Si este miembro no es 0, especifica el número de bytes que se deben mantener de cada fotograma recibido.</span><span class="sxs-lookup"><span data-stu-id="bfd69-139">If this member is not 0, then it specifies how many bytes to keep of each frame received.</span></span> <span data-ttu-id="bfd69-140">Si es 0, mantenga todo el marco.</span><span class="sxs-lookup"><span data-stu-id="bfd69-140">If it is 0, then keep the whole frame.</span></span>

</dd> <dt>

<span data-ttu-id="bfd69-141">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="bfd69-141">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="bfd69-142">Reservado.</span><span class="sxs-lookup"><span data-stu-id="bfd69-142">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bfd69-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfd69-143">Remarks</span></span>

<span data-ttu-id="bfd69-144">La combinación de marcas, valores y expresiones determina qué fotogramas pasará el controlador que utiliza estos datos de estructura.</span><span class="sxs-lookup"><span data-stu-id="bfd69-144">The combination of flags, values, and expressions determine which frames will be passed by the driver that uses this structure data.</span></span> <span data-ttu-id="bfd69-145">Para obtener más información sobre la implementación de una estructura **CAPTUREFILTER** , consulte [filtros de captura](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="bfd69-145">For more information about implementing a **CAPTUREFILTER** structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bfd69-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfd69-146">Requirements</span></span>



| <span data-ttu-id="bfd69-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfd69-147">Requirement</span></span> | <span data-ttu-id="bfd69-148">Value</span><span class="sxs-lookup"><span data-stu-id="bfd69-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bfd69-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfd69-149">Minimum supported client</span></span><br/> | <span data-ttu-id="bfd69-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bfd69-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bfd69-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfd69-151">Minimum supported server</span></span><br/> | <span data-ttu-id="bfd69-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bfd69-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bfd69-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfd69-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfd69-154"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfd69-154"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfd69-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfd69-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfd69-156">ADDRESSTABLE</span><span class="sxs-lookup"><span data-stu-id="bfd69-156">ADDRESSTABLE</span></span>](addresstable.md)
</dt> <dt>

[<span data-ttu-id="bfd69-157">ADDRESSPAIR</span><span class="sxs-lookup"><span data-stu-id="bfd69-157">ADDRESSPAIR</span></span>](addresspair.md)
</dt> <dt>

[<span data-ttu-id="bfd69-158">Expresiones</span><span class="sxs-lookup"><span data-stu-id="bfd69-158">EXPRESSION</span></span>](expression.md)
</dt> <dt>

[<span data-ttu-id="bfd69-159">ANDEXP</span><span class="sxs-lookup"><span data-stu-id="bfd69-159">ANDEXP</span></span>](andexp.md)
</dt> <dt>

[<span data-ttu-id="bfd69-160">PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="bfd69-160">PATTERNMATCH</span></span>](patternmatch.md)
</dt> </dl>

 

 




